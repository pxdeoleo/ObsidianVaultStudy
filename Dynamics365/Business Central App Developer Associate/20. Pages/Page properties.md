>[!summary]
[[Pages Overview|Page]] properties in [[Business Central]] are essential parameters that define the characteristics and behavior of a page. Each page must have an ID and Name, and other properties such as Caption, PageType, SourceTable, and DataAccessIntent to configure its functionality.

#### Definitions
- **ID and Name**: Unique identifiers for pages. The ID must be within the range provided by Microsoft to avoid conflicts. The Name should follow a structured format and include a prefix or suffix for uniqueness.

>[!info] Page Structure

The definition of a table in AL includes the ID and Name:
```
page [ID] [Name]
```
Example of a page structure in AL.

>[!info] Caption Property

- **Caption**: Text displayed in the title bar of the window.

>[!info] PageType Property

- **PageType**: Defines the layout of the window (e.g., Card or List).

>[!info] CardPageId Property

- **CardPageId**: Indicates the page to display when a user selects a record in a list.

>[!info] SourceTable and SourceTableView Properties

- **SourceTable**: Defines the table for which the page will display records.
- **SourceTableView**: Allows sorting and filtering of SourceTable records.

>[!info] Editable Property

- **Editable**: Defines if users can make changes to records on the page. Default is Yes.

>[!info] InsertAllowed, ModifyAllowed, DeleteAllowed Properties

- **InsertAllowed, ModifyAllowed, DeleteAllowed**: Control whether users can insert, modify, or delete records. Default is Yes for all.

>[!info] DataAccessIntent Property

- **DataAccessIntent**: Can be ReadOnly or ReadWrite. It hints the server to connect to a secondary replica if possible. ReadOnly improves performance but prevents modifications.

#### Tags
#BusinessCentral #pageproperties #AL #Dynamics365 #development #configuration