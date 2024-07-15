>[!summary]
Page Extension objects in Business Central extend existing pages, allowing for modifications such as adding new fields or modifying properties of existing ones. However, not all properties can be changed, and existing fields cannot be deleted, only hidden.

#### Definitions
- **Page Extension Object**: Used to extend existing pages in the Business Central application.

>[!info] Key Points

- **Modification Limits**: You can modify some page properties but not ID and Name properties. 
- **Field Handling**: You can add new fields, modify properties of existing fields, but can't delete fields; set the Visible property to false to hide them.

>[!example] Creating a Page Extension

1. **Create Page Extension**: Use the `tpageext` snippet.
2. **Define Layout**: Specify fields to add or existing fields to move/modify.

>[!tip] Layout Keywords

- **addfirst(anchor)**: Adds control at the first position within a specified container.
- **addlast(anchor)**: Adds control at the last position within a specified container.
- **addafter(anchor)**: Adds control directly after a specified group/control.
- **addbefore(anchor)**: Adds control directly before a specified group/control.
- **modify(name)**: Modifies properties of an existing control.
- **movefirst(anchor; controls)**: Moves specified control(s) to the first position within a container.
- **movelast(anchor; controls)**: Moves specified control(s) to the last position within a container.
- **moveafter(anchor; controls)**: Moves specified control(s) directly after a specified anchor.
- **movebefore(anchor; controls)**: Moves specified control(s) directly before a specified anchor.

>[!info] Naming Conventions

- **Unique Names**: Use a prefix or suffix for unique object names.
- **Field/Action Names**: Each field or action in the page extension must have a unique prefix or suffix.

>[!example] Sample AL Page Extension

- **Scenario**: Extending the Customer Card page by adding Facebook and Twitter fields through a table extension and moving the Email field after Twitter.
```al
pageextension 50100 MyCustomerCardExt extends "Customer Card"
{
    layout
    {
        addlast("General")
        {
            group("Social Media")
            {
                field(Facebook; "Facebook")
                {
                    ApplicationArea = All;
                }
                field(Twitter; "Twitter")
                {
                    ApplicationArea = All;
                }
            }
        }
        moveafter("Twitter")
        {
            field("Email")
            {
                ApplicationArea = All;
            }
        }
    }
}
```

#### Tags
#PageExtension #BusinessCentral #AL #Development #Customization