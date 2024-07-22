>[!summary]
Excel [[Built-in Report layouts|report layouts]] in Microsoft Dynamics 365 Business Central allow end-users to modify and design reports using Excel's capabilities. This flexibility enables users to customize the look and feel of reports, add views, and use features like pivot tables and charts.

#### Definitions
- **Excel Report Layout:** A report layout based on an Excel (.xlsx) file that users can modify to customize report designs.
- **Data Contract:** Defines the metadata fields from the dataset definition that the layout uses.

>[!example] Example Report
```al
report 50101 ExampleEXCELLayout
{
    Caption = 'ExampleEXCELLayout';
    UsageCategory = ReportsAndAnalysis;
    ApplicationArea = All;
    DefaultRenderingLayout = ExampleEXCELLayout;

    dataset
    {
        dataitem(Customer; Customer)
        {
            column(CustomerNo; "No.") { }
            column(CustomerName; Name) { }
            column(City; City) { }
            column(BalanceLCY; "Balance (LCY)") { }
        }
    }

    rendering
    {
        layout(ExampleEXCELLayout)
        {
            Type = Excel;
            LayoutFile = './src/Reports/EXCEL/ExampleEXCELLayout.xlsx';
            Caption = 'ExampleEXCELLayout';
            Summary = 'An example of an EXCEL Layout.';
        }
    }
}
```

>[!info] Adding Layouts
- Use the rendering section of a report object to enable multiple layouts.
- Specify details like layout file path, caption, and summary in the layout section.

>[!example] Steps to Create Excel Report Layout
1. **Set Up Excel Layout:**
   - Open Visual Studio Code and build the extension (Ctrl+Shift+B) to generate the ExampleEXCELLayout.xlsx file.
   - Right-click the generated file and select Open Externally.

2. **Edit in Microsoft Excel:**
   - Ensure the dataset remains unchanged; only modify the layout.
   - Use the Insert tab to create PivotTables and charts.
   - For PivotTables, use the PivotTable Fields pane to select fields and configure values (e.g., sum of BalanceLCY).

3. **Save and Run Report:**
   - Save and close the Excel file.
   - In Visual Studio Code, press Ctrl+F5 to compile and run the report in Business Central.
   - Search for the Report Layout Selection page, select the report, and choose Excel as the Layout Type.
   - Run the report and download the generated Excel file.

4. **Modify Data Contract:**
   - Ensure the Data worksheet defines metadata fields in the first row.
   - Use the ExcelLayoutMultipleDataSheets property for multiple worksheets in the dataset.

>[!info] Data Contract Rules
- Metadata fields must be written in the first row of the Data worksheet.
- Fields must match metadata fields in the dataset definition.
- Demo data can be added for easier troubleshooting but will be removed upon import to Business Central.

#### Tags
#reporting #dynamics365 #businesscentral #excel #layouts #datacontract #pivot_tables #charts