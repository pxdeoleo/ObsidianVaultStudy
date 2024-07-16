>[!summary]
The [[Business Central]] Performance Toolkit helps track and compare performance between different builds of your solutions to ensure code changes don't negatively impact performance in customer tenants.

#### Definitions
- Performance tracking tool for Business Central solutions and customizations.

>[!info] Importance
Business Central often serves as a scalable platform for ISVs and VARs to deliver solutions and customizations. Keeping performance levels high ensures customer satisfaction and efficient operation.

>[!info] Usage Scenarios
The toolkit helps consultants simulate loads to gain confidence in Business Central's ability to support specific customer loads during onboarding.

>[!info] Extensions
The toolkit includes two extensions:
1. **Business Central Performance Toolkit** (available on AppSource)
2. **Business Central Performance Toolkit Samples** (available on GitHub)

>[!info] Environment
- The toolkit can only be used in sandbox environments and Docker images, not in production tenants.

#### Installing the Performance Toolkit Extension
1. Open the Extension Management page in your Sandbox environment.
2. Select **Manage** > **Extension Market Place**.
3. Search for **Performance Toolkit** and select **Get it now**.
4. Enter your information and select **Continue**.
5. Select **Install** and confirm with **Ok**.
6. The Performance Toolkit is now installed.

#### Installing the Performance Toolkit Samples
1. Create a new AL project in VSCode.
2. Set dependencies in `app.json`.
3. Download the `src` folder from the BCPT-SampleTests GitHub repository.
4. Renumber objects in the `src` folder to your range (e.g., [50.000..99.9999]).
5. Renumber enum values in `TestCodeunitsWithParams.Enum.al`.
6. Deploy the extension to your Sandbox.

#### Toolkit Features
- **Framework for test scenarios**: Define tests to run in parallel, log results, and import/export suite definitions.
- **Predefined test suites**: Cover basic scenarios and inspire custom suites for customer environments.
- **Command line tool**: Simulate multiple users and run concurrent client sessions.

#### Running Tests
- **Multiple Sessions**: Typically run suites for multiple sessions using the **Start** action.
- **Single Run Mode**: For lightweight testing, use **Start in Single Run mode** to run the suite once and quickly identify regressions.

#### Configuring a Suite
1. Search for **BCPT Suites** and select the related link.
2. Select **New** to create a suite.
3. Provide identifier, description, and tag for the test.
4. Define timing and user delays.
5. Specify the base version for comparison.
6. Configure lines for the suite, including codeunits, parameters, and number of sessions.
7. Use **Run in Foreground** for sequential tests.

#### Starting the Run from PowerShell
1. Create the credential object:
    ```powershell
    $Credential = New-Object PSCredential -ArgumentList <user email>,(ConvertTo-SecureString -String <password> -AsPlainText -Force)
    ```
2. Start tests in a Business Central online sandbox:
    ```powershell
    RunBCPTTests.ps1 -Environment PROD -AuthorizationType AAD -Credential $Credential -SandboxName <sandbox name> -TestRunnerPage 149002 -SuiteCode "TRADE-50U"
    ```
3. View results on the BCPT Suite Lines FastTab and use filters to troubleshoot errors.

#### Example: Single Run Mode for PRT
1. Create a new suite on the **BCPT Suites** page.
2. Provide a name and tag for the suite.
3. Configure the suite lines with the necessary test.
4. Select **Start in Single Run mode**.
5. View results and set the baseline in the **Log Entries** page.

#### Tags
#performance #businescentral #toolkit #isv #var #customizations #sandbox #regressiontesting