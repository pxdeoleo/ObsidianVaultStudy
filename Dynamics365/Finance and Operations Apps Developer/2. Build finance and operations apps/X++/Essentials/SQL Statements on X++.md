>[!summary]
>SQL statements in X++ enable manipulation of data within the Dynamics 365 database, including operations like selecting, inserting, updating, and deleting records.

#### Definitions
- **SQL Statements**: Commands that allow interaction with database records in X++, such as selecting, inserting, updating, or deleting data.

>[!info] Using SQL Statements in X++
- **Select**: Retrieves data from the database.
- **Insert**: Adds new records to a table.
- **Update**: Modifies existing records.
- **Delete**: Removes records from a table.

>[!bug] Common Pitfalls
- Using `select *` is not recommended because it can degrade performance by retrieving unnecessary data.

>[!info] Key SQL Operations
- **Select Statement**: Specifies what data to retrieve, from which tables, and under what conditions.
  - Example: `Select AccountNum from CustTable where AccountNum > '1000';`
- **Join Clause**: Combines rows from two or more tables based on a related column.
  - Example: `Select * from SalesLine join SalesTable on SalesLine.SalesId == SalesTable.SalesId;`
- **Insert Recordset**: Inserts multiple records into a table from another table.
  - Example: `insert_recordset myTable (myNum) select myNum from anotherTable;`
- **Update Recordset**: Updates multiple records in a table.
  - Example: `update_recordset salesLine setting unitPrice = 10 where salesId =='S0001';`
- **Delete From**: Deletes multiple records from a table.
  - Example: `delete_from salesLine where salesLine.salesId == 'S0001';`

>[!tip] Effective Data Handling
- Always use `forUpdate` in select statements when planning to update the data to lock the records and prevent data inconsistency.

>[!example] Complex SQL Operations
- **Complex Select with Sorting and Filtering**:
  ```x++
  Select forUpdate CustTable order by AccountNum desc
    where custTable.accountNum > '1000'
    && custTable.accountNum < '2000';
  ```
- **Iterative Data Manipulation**:
  ```x++
  While select forUpdate * from CustTable 
    order by AccountNum desc
    where custTable.accountNum > '1000'
    && custTable.accountNum < '2000'
  {
      // Additional logic here
  }
  ```
  