>[!summary]
>SQL Insights provides comprehensive monitoring tools in [[Lifecycle Services]] to analyze and enhance SQL performance within specific environments.

#### Definitions
- SQL Insights: A suite of tools for monitoring SQL performance metrics, available on the [[Lifecycle Services]] platform.

>[!info] SQL Insights Overview

SQL Insights in [[Lifecycle Services]] offers a detailed view of database performance, including metrics on queries, indexes, and real-time operations, accessible through the Environment Monitoring page.

>[!bug] Handling Query Time-outs

When running performance queries, ensure that the 'Use Fast Query' option is turned off if time-outs occur, allowing for more stable query execution.

>[!info] Monitoring Tools

Located under the SQL Insights tab, tools such as Performance Metrics, Index Analysis, and Live View provide real-time and historical data to aid in performance tuning.

>[!tip] Utilizing Index Analysis

Use Index Analysis to assess the efficiency of table indexing and make adjustments based on trends and performance metrics, enhancing overall database performance.

>[!attention] SQL Performance Actions

Predefined actions like index management and query termination are crucial for maintaining optimal performance in both sandbox and production environments.

>[!example] Analyze Query Performance

1. Navigate to the SQL Insights tab on the Environment Monitoring page.
2. Select the Performance Metrics section.
3. Review the most expensive queries and their details.
4. Download the query execution plan for deeper analysis.
5. Implement recommended actions based on insights gained.

>[!info] Advanced Troubleshooting

For deeper analysis, predefined queries help retrieve detailed logs for specific issues such as slow queries or deadlocks, facilitating targeted troubleshooting efforts.

>[!info] Tool Legacy and Advancements

SQL Insights' capabilities are an evolution of the DynPerf tool from Microsoft Dynamics AX 2012, offering advanced diagnostic and monitoring features for modern SQL environments.