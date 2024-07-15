>[!summary]
The TableRelation property in Dynamics 365 [[Business Central]] is used to establish relations between tables, facilitating lookups and drop-down menus for linked values. It supports regular, filtered, and conditional table relations to provide dynamic data connectivity and filtering.

#### Definitions
- **TableRelation property**: A property used to define the relationship between two tables, enabling lookups and dropdown menus for user selection.

#### Types of Table Relations
>[!info] Regular Table Relation
- Establishes a simple link to another table.
- Automatically links to the primary key of the specified table.
- Example: Customer table linking to the primary key of the Country table.

>[!info] Filtered Table Relation
- Limits the records shown from the linked table using filters.
- Displays a subset of records based on specified criteria.
- Example: Filtering Country/Region codes to show only non-blank EU Country/Region codes.

>[!info] Conditional Table Relation
- Creates a dynamic relationship based on conditions.
- Links to different tables depending on the evaluation of a condition.
- Example: Sales Line table linking to different tables (e.g., Items or Resources) based on the Type field value.

#### Implementation Examples
>[!example] Example Code Snippet for Conditional Table Relation
- **Sales Line Table (Table 37)**:
    ```al
    field(No.; Code[20])
    {
        TableRelation = 
            if (Type = const(Item)) Item
            else if (Type = const(Resource)) Resource;
    }
    ```

#### Enhancements
>[!tip] Use Option Access Syntax in Formulas
- Improves readability and maintainability by removing hard-coded integer IDs.
- Allows using option names instead of integer IDs in properties like SourceTableViews and TableRelations.
- Example:
    ```al
    // Old way using integer ID
    SourceTableView = where("Source Type" = const(18));

    // New way using option name
    SourceTableView = where("Source Type" = const(Database::Customer));
    ```

#### Tags
#TableRelation #Dynamics365 #BusinessCentral #DatabaseRelations #FilteredRelations #ConditionalRelations