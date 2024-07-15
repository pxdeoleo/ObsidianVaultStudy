> [!summary] 
> Field groups are special sets of properties on the table level used to define which fields of a linked table should be displayed to the user in different contexts, such as drop-down menus or tile lists.
#### Definitions
- **Field Groups**: Sets of properties at the table level defining fields displayed in linked tables.

> [!info] Field Groups in Drop-Down Menus
- Used to specify fields shown when a table is called through a relation.
- Default fields: **No.** and **Name**.
- Other fields can be specified as needed.

> [!info] DropDown FieldGroup
- Defines fields displayed in a drop-down menu.
- Default: **No.** and **Name** fields.

> [!info] Brick FieldGroup
- Displays a list in tile format.
- Example: Customer List.

> [!info] Brick Layout
- Dynamic layout changes based on the number of columns.
- Positions: Six possible field positions.

> [!tip] Displaying Images in Brick Layout
- Field types: **Media**, **MediaSet**, or **BLOB**.
- Last field in field group automatically displays images.

> [!info] [[Defining Field Groups]] in AL
- Defined under the **keys** section in AL.

#### Tags
#fieldgroups #dropdown #bricklayout #AL #tableproperties

