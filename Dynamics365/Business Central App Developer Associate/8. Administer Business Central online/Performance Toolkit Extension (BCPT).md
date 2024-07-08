> [!summary] The Performance Toolkit (BCPT) is designed for ISVs and VARs to test the performance of Business Central solutions across different versions and user volumes. It helps simulate realistic workloads to compare performance between builds of their solutions.

#### Definitions

- **Test suite**: Configuration of test codeunits, parameters, concurrent sessions, and scenario duration.
- **Test suite tag**: Tags for test suites to compare results between different configurations or versions.
- **Test codeunit**: Containers for test scenarios.
- **Test codeunit parameter**: Parameters to modify test behavior, such as number of sales lines.
- **Test scenario**: Defined using StartScenario/EndScenario within test codeunits, logs context and results.
- **Test suite run**: Logged results of a test suite run, used for performance comparisons.
- **Test suite baseline (run)**: A chosen scenario run for comparison with other runs.

> [!info] Performance Toolkit Components

- **Performance Toolkit**: Free extension on Visual Studio Code Extensions Marketplace. Sets up BCPT projects, includes sample tests, and PowerShell scripts.
- **PowerShell Scripts**: Command line tool for simulating user interactions.
- **BCPT-SampleTests**: Free sample tests available on GitHub for inspiration.

> [!info] Usage Limitations

- Usable only in sandbox environments and Docker images, not in production tenants.
- Currently supported only on Windows.

> [!example] Steps to Get Started

1. Install the Performance Toolkit extension in Visual Studio Code.
2. Set up the BCPT project and Performance Toolkit extension.
3. Write test scenarios.
4. Configure a BCPT suite in Business Central.

> [!tip] Installing the Extension in Visual Studio Code

1. Open the Extension Marketplace, search for Performance Toolkit, and install.
2. Create a project with the BCPT Setup command.
3. Choose testing environment (Docker or SaaS).
4. Sign in to Business Central, select environment, and specify project directory.
5. Verify and install required components:
    - Performance Toolkit
    - Sample test cases
    - PowerShell scripts

> [!info] Writing Test Scenarios

- **Normal codeunit subtype**: Define scenarios in OnRun trigger for scenarios without pages.
- **Test codeunit subtype**: Use Test Pages for realistic client interactions.
- Use StartScenario/EndScenario for logging and UserWait() for simulating user delays and commits.

> [!example] Sample Test Codeunit: Normal Subtype

```AL
codeunit 50000 "Create Sales Order"
{
    var
        BCPTTestContext: Codeunit "BCPT Test Context";
    trigger OnRun();
    var
        Customer: Record Customer;
        SalesHeader: Record "Sales Header";
    begin
        Customer.FindFirst();
        SalesHeader.Init();
        SalesHeader."Document Type" := SalesHeader."Document Type"::Order;
        SalesHeader.Insert(true);
        BCPTTestContext.EndScenario('Add Order');
        BCPTTestContext.UserWait();
        BCPTTestContext.StartScenario('Enter Account No.');
        SalesHeader.Validate("Sell-to Customer No.", Customer."No.");
        SalesHeader.Modify(true);
        BCPTTestContext.EndScenario('Enter Account No.');
        BCPTTestContext.UserWait();
    end;
}

```
>[!example] Sample Test Codeunit: Test Subtype

```AL
codeunit 50000 "Create Sales Order"
{
    Subtype = Test;
    var
        BCPTTestContext: Codeunit "BCPT Test Context";
    trigger OnRun();
    var
        Customer: Record Customer;
        SalesOrder: TestPage "Sales Order";
    begin
        Customer.FindFirst();
        SalesOrder.OpenNew();
        SalesOrder."No.".SetValue('');
        BCPTTestContext.EndScenario('Add Order');
        BCPTTestContext.UserWait();
        BCPTTestContext.StartScenario('Enter Account No.');
        SalesOrder."Sell-to Customer No.".SetValue(Customer."No.");
        BCPTTestContext.EndScenario('Enter Account No.');
        BCPTTestContext.UserWait();
    end;
}

```

> [!tip] Using Parameters in Tests

- Implement the `BCPT Test Param. Provider` interface to define and validate parameters.
- Extend `BCPT Test Param. Enum` to make parameters available in the toolkit.

```AL
codeunit 50000 "Create PO with N Lines" implements "BCPT Test Param. Provider"
{
    var
        BCPTTestContext: Codeunit "BCPT Test Context";
        NoOfLinesParamLbl: Label 'Lines';
        ParamValidationErr: Label 'Parameter is not defined in the correct format. The expected format is "%1"', Comment = '%1 = Format';
        NoOfLinesToCreate: Integer;
    trigger OnRun();
    begin
        ...
    end;
    procedure GetDefaultParameters(): Text[1000]
    begin
        exit(copystr(NoOfLinesParamLbl + '=' + Format(10), 1, 1000));
    end;
    procedure ValidateParameters(Parameters: Text[1000])
    begin
        if StrPos(Parameters, NoOfLinesParamLbl) > 0 then begin
            Parameters := DelStr(Parameters, 1, StrLen(NoOfLinesParamLbl + '='));
            if Evaluate(NoOfLinesToCreate, Parameters) then
                exit;
        end;
        Error(ParamValidationErr, GetDefaultParameters());
    end;
}
```

```AL
enumextension 50000 "Test Codeunits with Params" extends "BCPT Test Param. Enum"
{
    value(50000; "50000")
    {
        Implementation = "BCPT Test Param. Provider" = "Create PO with N Lines";
    }
}
```
