>[!summary]
>Creating and modifying data sources is crucial for [[Reporting]] tools like [[SQL Server Reporting Services]] (SSRS) and Power BI, enabling them to pull relevant data for insightful reporting.

#### Definitions
- Data Sources: Configurations within [[Reporting tools]] that define where and how data is retrieved for reports.

>[!info] SSRS Data Sources

SSRS utilizes data sources connected through Visual Studio to feed data into reports, using different types of sources based on the complexity and requirements of the report.

>[!bug] Data Source Limitations

Modifications to SSRS data sources may require extensions to existing tables or RDP (Report Data Provider) classes to accommodate new data needs or changes.

>[!info] Types of SSRS Data Sources

- **Query**: Directly uses SQL queries for data retrieval.
- **Business Logic**: Accesses data outside standard finance and operations apps.
- **Report Data Provider Class**: Combines queries with additional logic for complex data processing.
- **Enum Provider**: Filters data based on enumerated types, useful for parameterized reports.

>[!tip] Efficient Data Source Management

For SSRS, ensure that the correct type of data source is chosen to optimize report performance and accuracy.

>[!attention] Power BI Connection Process

Connecting Power BI to a data source involves selecting the data type, establishing a connection, and optionally editing the data query to refine the data set.

>[!example] Connecting to a Data Source in Power BI

1. Open Power BI and click the "Get Data" button on the toolbar.
2. Explore and select from the available data sources or search for additional ones.
3. Connect to the chosen data source by entering necessary credentials and confirming the connection.
4. Use the Navigator to either load the data directly or edit the query to adjust the data set before loading.

>[!info] Power BI Data Sources

Power BI offers a wide array of data connections, from simple file-based sources to complex databases and online services, facilitating versatile data integration for dynamic reporting and analysis.