>[!summary]
The TableExtension object is utilized to extend existing tables in the [[Business Central]] application. It allows for the addition of new fields and secondary keys while imposing certain restrictions on modifications.

#### Definitions
- **TableExtension Object**: An object used to extend the capabilities of existing tables in Business Central without altering their core properties or structure.

>[!info] Key Points

1. **Modification Limits**: 
   - Cannot change `ID` and `Name` properties of the table.
   - Cannot delete existing fields.
   - Cannot change the length of fields of type `Text` or `Code`.
   - Can create new secondary keys but cannot modify or remove existing keys.

2. **Field Management**:
   - New fields can be added using the `tfield` snippet.
   - Existing fields can be modified using the `modify` keyword, though no snippet exists for this action.

3. **Naming Conventions**:
   - Each table extension requires a unique name, recommended to include a prefix or suffix.
   - Each field within the extension should also have a prefix or suffix to maintain uniqueness.

>[!example] Basic Example of Table Extension in AL
```al
tableextension 50100 MyCustomerExtension extends Customer
{
    fields
    {
        field(50100; "New Field"; Text[50])
        {
            DataClassification = ToBeClassified;
        }
    }
    modify("Existing Field")
    {
        DataClassification = ToBeClassified;
    }
}
```

>[!tip] Creating [[Table Extensions]]
- Use the `ttableext` snippet to create a table extension.
- Use the `tfield` snippet to add new fields to the table extension.

#### Tags
#TableExtension #BusinessCentral #Dynamics365 #AL #Development