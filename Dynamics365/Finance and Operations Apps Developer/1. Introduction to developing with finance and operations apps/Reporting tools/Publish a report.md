>[!summary]
>Deploying SSRS reports is a crucial step in making them accessible within finance and operations apps, with options to deploy from both Visual Studio and PowerShell.

#### Definitions
- SSRS ([[SQL Server Reporting Services]]): A server-based report generating software system used in conjunction with Microsoft SQL Server.

>[!info] Deployment Methods

SSRS reports can be deployed directly from Visual Studio or using PowerShell scripts, depending on the environment and access restrictions.

>[!bug] Deployment Risks

Avoid deploying reports directly via PowerShell in production environments to prevent potential disruptions and maintain system integrity.

>[!info] PowerShell Deployment

PowerShell allows for the deployment of individual reports or all reports within a package, useful in environments lacking Visual Studio access.

>[!tip] Visual Studio Deployment

For environments with access to Visual Studio, deploying reports directly through the IDE is straightforward and integrates seamlessly with report development workflows.

>[!attention] Environment Considerations

When deploying reports, be mindful of the specific server environment and drive configurations, as paths may vary (e.g., C:\, L:\, K:\).

>[!example] Deploying Reports

1. **From Visual Studio**:
   - Navigate to the report in Solution Explorer.
   - Right-click the report and select "Deploy" to deploy directly to the configured SSRS server.

2. **From PowerShell**:
   - To deploy all reports:  
     ```powershell
     C:\AosService\PackagesLocalDirectory\Plugins\AxReportVmRoleStartupTask\DeployAllReportsToSSRS.ps1 -PackageInstallLocation "C:\AosService\PackagesLocalDirectory"
     ```
   - To deploy a specific report:
     ```powershell
     C:\AosService\PackagesLocalDirectory\Plugins\AxReportVmRoleStartupTask\DeployAllReportsToSSRS.ps1 -Module ApplicationSuite -ReportName TaxVatRegister.Report
     ```

>[!info] Deployment Best Practices

Ensure that the deployment method aligns with the environment's security protocols and access limitations to maintain operational security and efficiency.