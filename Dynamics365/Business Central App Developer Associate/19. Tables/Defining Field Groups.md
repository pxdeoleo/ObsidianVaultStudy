>[!summary]
Field groups in table or table extension objects define the fields to display in drop-down controls on pages using the table, facilitating data presentation and user interaction.
#### Definitions
- **Field Group**: Defines the fields displayed in a drop-down control or tile view on a page.
- **DropDown**: Field group name used for adding fields to the drop-down control.
- **Brick**: Field group name used for displaying data as tiles.

>[!info] Syntax and Usage

- In a table object, field groups are defined using the `fieldgroups` control with the `fieldgroup(<Name>; <Field>)` keyword.
- `<Name>`: Either `DropDown` or `Brick`.
- `<Field>`: Comma-separated list of field names.

```al-language
fieldgroups
{
  fieldgroup(DropDown; Field1, Field2) { }
  fieldgroup(Brick; Field1, Field2) { }
}
```

- The `fieldgroups` keyword cannot be placed before the `key` control.
- The `DropDown` keyword must be capitalized correctly.

>[!info] [[Table Extensions]]

- In table extensions, use `addlast(<name>; <field>)` to add fields to existing field groups.
- The server removes duplicate fields if multiple extensions attempt to add the same field.
- A field can only be added to a field group once.

```al-language
tableextension 50100 CustomerExercise extends Customer
{
    fields
    {
        field(50100; "V02Max"; Decimal) { }
    }
   
    fieldgroups
    {
        addlast(DropDown; V02Max) { }
    }
}
```

- Fields added to a `DropDown` field group will not appear if `Visibility` is set to `false` on the underlying lookup page.

```al-language
tableextension 50101 ShipToAddressExercise extends "Ship-to Address"
{
    fieldgroups
    {
        addlast(DropDown; "Address 2") { }
    }
}

pageextension 50101 ShipToAddressExercise extends "Ship-to Address"
{
    layout
    {
        modify("Address 2")
        {
            Visible = true;
        }
    }
}
```

>[!tip] Predefined Field Groups

- Fields can always be added to the predefined `DropDown` and `Brick` field groups.
- If not defined on the target table, these groups are dynamically created and contain only the specified fields.
- Field order is determined by the server load order, removing duplicates.
#### Tags
#ALLanguage #BusinessCentral #FieldGroups #DropDown #Brick #TableExtension #Dynamics365