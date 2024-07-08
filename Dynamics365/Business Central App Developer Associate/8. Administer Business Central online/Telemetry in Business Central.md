> [!summary] 
> Telemetry in Business Central can be enabled at both the environment level and the app/extension level, allowing for comprehensive tracking and analysis of system performance, errors, and usage.

#### Definitions

- **Environment-level telemetry:** Enabled for a Business Central environment or on-premises server instance, sending data to an Azure Application Insights resource.
- **App/extension-level telemetry:** Enabled per-extension by setting an Azure Application Insights connection string in the app’s manifest, targeting publishers for detailed usage and performance insights.

> [!info] Telemetry Levels

- **Environment-level telemetry:** Gathers data on all operations in a Business Central environment.
- **App/extension-level telemetry:** Captures events specific to the app/extension, aiding publishers in understanding app performance and usage.

> [!example] Enabling Environment Telemetry

1. Obtain Azure Application Insights resource and connection string.
2. **For Business Central Online:**
    - Use the admin center or admin center API.
3. **For Business Central On-premises:**
    - **Single-tenant:** Set Application Insights Connection String or Instrumentation Key.
    - **Multi-tenant:** Enable per-tenant telemetry when mounting tenants.
4. **Using BcContainerHelper:**
    - Specify the instrumentation key during container creation.

> [!info] Custom Telemetry Messages

- Craft custom telemetry messages using the LogMessage Method in AL.

> [!tip] Assigning Telemetry ID to Users

1. Sign in to Business Central as an administrator.
2. Navigate to Users via the search icon.
3. Open the User Card page.
4. Set the Telemetry ID field.

> [!example] Analyzing and Monitoring Telemetry with Power BI

1. **Install Power BI apps from Microsoft AppSource:**
    - **For environment telemetry:** Go to [bctelemetryreport](https://aka.ms/bctelemetryreport).
    - **For app telemetry:** Go to [bctelemetry-isv-app](https://aka.ms/bctelemetry-isv-app).
2. Follow instructions to install the app.
3. Open the app from the Power BI Apps section.

#### Telemetry Reports in Power BI

> [!info] Usage Report Provides 
> Insights into how Business Central is used, including sessions, clients, locations, page views, reports, feature usage, integrations, and deprecated features.

> [!info] Error Report 
> Analyzes user, integration, and system errors, complementing Jupyter notebook troubleshooting guides.

> [!info] Performance Report 
> Examines session statistics, OnCompanyOpen timings, page views, report timings, long-running SQL queries, database lock timeouts, long-running AL methods, web service calls, job queue timings, configuration packages, and app updates.

> [!info] Administration Report 
> Tracks environment inventory, update planning, and changes to environments, companies, extensions, indexes, and fields. Monitors retention policy data deletions.