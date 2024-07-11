> [!summary] [[Business Central]] emits telemetry data for various activities and operations on tenants and extensions. Telemetry can be sent to Application Insights for analysis, allowing for monitoring of tenant activities and diagnosing performance issues.

#### Definitions

- **Application Insights**: A service within Azure that collects telemetry data for analysis and presentation.
- **Telemetry**: Data that provides insights into the activities and health of your tenants.

> [!info] Enabling Application Insights

Application Insights can be enabled on two levels: tenant and extension.

- **Tenant level**: Gathers data on tenant-wide operations.
- **Extension level**: Targets specific events related to an extension.

Steps to enable Application Insights:

1. Get a Microsoft Azure subscription.
2. Create an Application Insights resource in Azure.
3. Copy the instrumentation key from the Application Insights resource.
4. In the Business Central administration center, select the environment to change.
5. Enable Application Insights and enter the instrumentation key.
6. Save and restart the environment.

> [!example] Viewing Telemetry Data in Application Insights

Telemetry data is stored in Azure Monitor Logs. To view data:

1. Open the Application Insights resource in the Azure portal.
2. Select Logs in the Monitoring menu.
3. Write log queries in Kusto query language (KQL).
```kql
traces
| take 100
| sort by timestamp desc

```
> [!info] Available Telemetry Signals

- Long running SQL queries
- Authorization attempts
- Web service requests
- Report execution
- Company lifecycle events
- Database lock timeouts
- Extension lifecycle events

> [!info] Custom Dimensions
> 

Each trace includes a `customDimensions` column with metrics specific to the trace. Each custom dimension is limited to 8000 characters, with excess characters stored in additional dimensions.

> [!info] Power BI Integration
> 

Power BI apps are available for analyzing telemetry data:

- **Environment telemetry**
- **App/Extension telemetry**

Steps to connect Power BI to Application Insights:

1. Get the Application Insights Application ID from Azure.
2. In Power BI, connect to Dynamics 365 Business Central Usage app.
3. Enter the Application Insights Application ID and lookback period.
4. Sign in and configure additional parameters if needed.
5. Refresh the dataset to update the data shown in the app.