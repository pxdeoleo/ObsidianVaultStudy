>[!summary]
>Adding columns to data items in reports involves specifying fields, variables, or expressions. It impacts report performance and requires unique naming for each column and data item.

#### Definitions
- **Column**: Entity in a report corresponding to fields in a table, a variable, or an expression.

>[!info] Column Types

Columns can be:
- A field in a table
- A variable
- An expression

>[!example] Adding a Column
Use the `tcolumn` snippet to add a column:
```al-language
column(ColumnName; SourceFieldName)
{
}
```
- **ColumnName**: Name you give to the column (must be CLS compliant).
- **SourceFieldName**: Name of the field in the table.

>[!tip] Best Practices
- Only add necessary columns to avoid increasing dataset size and negatively impacting performance.
- Each data item and column must have a unique `ColumnName`.

>[!example] Example
Fetching `No.`, `Name`, `City`, and `Balance LCY` columns from the Customer table:
```al-language
dataitem(Customer; Customer)
{
    column(No; "No.")
    {
    }
    column(Name; Name)
    {
    }
    column(City; City)
    {
    }
    column(BalanceLCY; "Balance (LCY)")
    {
    }
}
```

>[!info] Column Properties
- Use `Ctrl+Space` to view column properties.

#### Tags
#reports #columns #dataitem #performance #ALlanguage