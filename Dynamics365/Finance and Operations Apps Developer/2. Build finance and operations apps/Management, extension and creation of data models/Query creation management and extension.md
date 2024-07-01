>[!summary]
>Queries in Dynamics 365 Finance and Operations apps are powerful tools for retrieving and displaying data. They can be predefined or dynamically created and modified in code, optimizing data access in forms, reports, and views.

#### Definitions
- **Query**: A structured request to retrieve data, particularly useful in databases. In Dynamics 365, queries are built using the AOT (Application Object Tree).

>[!info] Creating and Managing Queries

To add a predefined query to a project:
1. Right-click the project in Solution Explorer.
2. Select Add > New Item.
3. Choose Data Model > Query.
4. Use the Designer and Properties windows to configure the query.

>[!bug] Common Issues in Query Configuration

Improper query configurations can lead to performance bottlenecks, especially if the queries retrieve excessive data or involve complex joins without proper indexing.

>[!info] Key Properties of Queries

- **Description**: Provides an overview of what the query does.
- **Interactive**: Indicates whether the query can prompt user interaction.
- **Allow Cross Company**: Allows queries to fetch data across different company accounts.

>[!tip] Best Practices for Query Performance

Use selective fields rather than "*" to improve SQL performance. Define indexes on tables that are frequently accessed by queries.

>[!attention] Extending Queries

While you cannot modify the core structure of a predefined query, you can extend its capabilities by:
- Adding new data sources or fields.
- Adjusting labels and properties.
- Enhancing sorting and grouping specifications.

>[!example] Modifying Queries in Code

Example of adding a range to a query programmatically:
```X++
public static void main(Args _args)
{
    Query query = new Query("MyCustTable");
    QueryBuildDataSource qbds;
    QueryBuildRange qbr;

    qbds = query.dataSourceTable(tableNum(CustTable));
    qbr = qbds.addRange(fieldNum(CustTable, CustGroup));

    QueryRun queryRun = new QueryRun(query);
    while (queryRun.next())
    {
        CustTable custTable = queryRun.get(tableNum(CustTable));
        info(strFmt("%1, %2", custTable.AccountNum, custTable.CustGroup));
    }
}
```
This code snippet creates a query for the `CustTable` and adds a filter on the `CustGroup` field.

>[!info] Using Queries in Applications

Queries are integral in driving data to forms and reports. They should be designed to balance flexibility with performance, ensuring they deliver the required data efficiently.

#### Extending Queries

To extend a query:
1. Find the query in Application Explorer.
2. Right-click the query and select Create extension.
3. Add modifications in the extension without altering the original query.

Extensions allow additional customization such as adding fields or data sources, and adjusting query properties like groupings and sort orders.

>[!info] Syncing and Building Queries

Always ensure that queries and their extensions are built and synchronized correctly to reflect changes in the database schema and avoid runtime errors.