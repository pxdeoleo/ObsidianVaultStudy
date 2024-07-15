> [!summary]
> Page controls in [[Business Central]] display data to the user, which can be from the database, AL expressions, images, static information, other pages, or control add-ins.

#### Definitions
- **Content area**: Largest part of a page, usually on the left, for fields, parts, etc.
- **FactBox area**: Smaller part of a page, usually on the right, for other page parts.
- **RoleCenter area**: Single area in a RoleCenter page for displaying role-specific information.
- **FastTabs**: Groups of fields on a Card page that can be collapsed or expanded.
- **Repeater**: Used in List pages to repeat records from a table.
- **Cue groups**: Used in Role Centers to show key data visually and provide filtered lists.
- **Fixed layout**: Multicolumn, read-only layout used for displaying statistics.

> [!info] Areas on a page
- Regular Card/List page: **Content area** (left), **FactBox area** (right)
- RoleCenter page: **RoleCenter area** only

> [!info] FastTabs on Card pages
- Used to group fields (e.g., General, Address & Contact, Invoicing, etc.)
- Defined as groups in AL

> [!info] Fields on List pages
- Use a **repeater** instead of groups to display records

> [!info] Cue groups
- Used in Role Centers to highlight key information
- Defined with `cuegroup` in AL
- **CueGroupLayout** property can be set to Wide for larger displays

> [!info] Fixed layout
- Used for statistics pages
- Displays fields in multicolumn, read-only format

#### Tags
#BusinessCentral #PageControls #AL #RoleCenters