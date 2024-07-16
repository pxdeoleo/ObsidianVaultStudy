
>[!summary]
The report design process is divided into two main phases: defining the logical structure (data model) and designing the visual elements. Additionally, it involves designing the Request page for user inputs before running the report.

#### Definitions
- **Logical Structure:** Defining the data model, which includes how data is collected and organized.
- **Visual Elements:** Designing the layout and presentation of the report.
- **Request Page:** A page where users enter options before running the report.

>[!info] Dataset Design
Designing the dataset is crucial as it determines which tables and fields are available in the report layout. It includes:
- Data items and columns
- Tables and their relationships
- Key, sort order, and filters
- Grouping and calculations

>[!info] Data Model
The data model involves:
- Defining data items (tables)
- Setting relationships between data items
- Configuring keys, sort orders, and filters
- Allowing user modifications at runtime
- Grouping data
- Calculating subtotals and totals

>[!example] Data Item Construct
A data item construct in AL language:
```al
dataitem(DataItemName; SourceTableName)
{

}
```
- **DataItemName:** A CLS-compliant name for the data item.
- **SourceTableName:** The name of the table.

>[!example] Multiple Data Items
Data items can be concatenated or nested:
- Concatenated example:
```al
dataset
{
    dataitem(Customer;Customer)
    {

    }
    dataitem(Vendor;Vendor)
    {

    }
}
```
- Nested example:
```al
dataset
{
    dataitem(Customer;Customer)
    {
        dataitem("Sales Line";"Sales Line")
        {
            DataItemLinkReference = Customer;
            DataItemLink = "Bill-to Customer No." = field("No.");
        }
    }
}
```
- **DataItemLinkReference:** Links to the parent data item.
- **DataItemLink:** Specifies the field linking parent and child data items.

>[!info] PrintOnlyIfDetail Property
Determines whether to print parent data item if child data item has no output:
- **true:** Similar to INNER JOIN
- **false:** Similar to LEFT OUTER JOIN (default)

Example:
```al
dataitem(Customer; Customer)
{
    PrintOnlyIfDetail = true;
    dataitem("Sales Line"; "Sales Line")
    {
        DataItemLinkReference = Customer;
        DataItemLink = "Bill-to Customer No." = field("No.");
    }
}
```

>[!tip] DataItemTableView Property
Sets key, sort order, and filters for data items:
```al
dataitem(Customer; Customer)
{
    PrintOnlyIfDetail = true;
    DataItemTableView = where(Blocked=filter(false));
}
```
- **Key:** Predefined sort key.
- **Sort Order:** Predefined sorting.
- **Filter:** Predefined filter (e.g., non-blocked customers).

>[!example] Keyboard Shortcut
Use `Ctrl+Space` in Visual Studio Code for an overview of available data item properties.

#### Tags
#reportdesign #datamodel #dataset #visualelements #requestpage #dataitems #ALlanguage #filters #sortorder #performance