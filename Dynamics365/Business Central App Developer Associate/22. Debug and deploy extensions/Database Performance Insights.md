>[!summary]
Developers and administrators can gain insights into database performance using Dynamic Management Views (DMVs) and Database Wait Statistics in [[Business Central]]. This allows them to analyze and optimize query performance.
#### Definitions
- **Dynamic Management Views (DMVs)**: Tools that provide performance counters and SQL query information for databases.
- **Database Wait Statistics**: Virtual table in Business Central showing data on database wait times, accessible through AL code.

>[!info] Performance Insights

- **DMVs**: Requires direct database access for performance data; not possible for Business Central online due to security.
- **Database Wait Statistics**: Makes wait data available as a virtual table in Business Central, viewable via a dedicated page.

>[!tip] Checking Performance

Use Database Wait Statistics to see how long queries wait and the reasons for the wait. Categories include CPU, Idle, Lock, Buffer IO, etc.

>[!example] Columns in Database Wait Statistics

1. **Wait Category Type**: Reasons for query wait (e.g., CPU, Idle, Lock).
2. **Wait Time Counters**: Wait Time in ms, Max Wait Time in ms, Signal Wait Time in ms.
3. **Waiting Tasks Count**: Total count of each wait category.
4. **Database Start Time**: Time when the database was started or restarted.

>[!attention] Data Characteristics

- Wait times are historical, not live. They show completed query wait times since the last database start or reset.

>[!info] Emitting Telemetry

- Emit data to telemetry and analyze it in Application Insights by selecting the Emit telemetry icon.

#### Tags
#databaseperformance #BusinessCentral #DMVs #waitstatistics #ALcode #telemetry