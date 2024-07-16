> [!summary]
> Building a [[Reports|report]] from data items involves creating a hierarchy of tables, allowing iteration through records in underlying tables to collect information. Proper structuring enables the creation of complex reports, such as listing customers and their sales orders.
#### Definitions
- **Data Item**: Represents a table in the report. Iterated for all records when the report runs.
- **Column**: Entity within a data item that can be a field, variable, expression, or caption.

> [!info] Report Data Model
- Data model of a report is built from data items (tables).
- Hierarchy of data items controls the data collection process.
- Indenting data items establishes relationships between them.

> [!example] Hierarchical Data Items
- **Customer Report**: 
  - Data item for the Customer table.
  - Indented data item for the Sales Order table.
- Process:
  1. Examine all customers in the Customer table.
  2. Examine all sales orders in the Sales Order table.
  3. Find sales orders related to each customer.

> [!info] Data Item Hierarchy
- Establish hierarchy by indenting data items.
- Controls how information is collected across multiple tables.

> [!info] Report Dataset
- Built from data items and columns.
- **Column Types**:
  - Field in a table.
  - Variable.
  - Expression.
  - Caption (unrelated to a specific table).

#### Tags
#reports #datamodel #dataitems #hierarchy #columns