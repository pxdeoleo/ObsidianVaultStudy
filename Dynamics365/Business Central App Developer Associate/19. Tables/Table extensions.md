> [!summary]
> Table extensions in [[Business Central]] allow for limited modification of table and field properties. They also support index tuning for performance improvement.

#### Definitions
- **Table Extensions**: Tools for modifying certain properties of base tables and fields in Business Central.
- **Index Tuning**: Optimization technique for handling performance issues due to data distributions.

>[!info] Modifiable Table Properties

- **Caption**: The text label for the table.
- **DataCaptionFields**: Fields used for data captions.
- **Description**: A brief description of the table.
- **DrillDownPageId**: The page ID for drill-down operations.
- **LookupPageId**: The page ID for lookup operations.

>[!info] Modifiable Field Properties

- **BlankZero**: Determines if zero values should be displayed as blank.
- **Caption**: The text label for the field.
- **CaptionClass**: Class used for generating captions.
- **Description**: A brief description of the field.
- **OptionCaption**: Captions for option-type fields.
- **TableRelation**: Relationship to another table.
- **Width**: Display width of the field on a page.

>[!info] Index Tuning

- Partners can add keys to tables and table extensions to address performance issues.
- **Normal and SIFT keys** are supported.
- Keys can be defined in both base tables and table extensions, with certain limitations.

#### Example Code
```al
table 50120 MyBaseTable
{
    fields
    {
        field(1; MyBaseField1; Integer)
        {
        }
        field(2; MyBaseField2; Integer)
        {
        }
    }

    keys
    {
        key(PK; MyBaseField1) //primary key
        {
            Clustered = true;
        }
        key(Key1; MyBaseField2) //secondary key
        {
        }
    }
}

tableextension 50121 MyBaseTableExt extends MyBaseTable
{
    fields
    {
        field(3; MyExtField1; Integer)
        {
        }
        field(4; MyExtField2; Integer)
        {
        }
    }

    keys
    {
        key(ExtKey1; MyExtField1) //secondary key
        {
        }
        key(ExtKey2; MyBaseField1, MyBaseField2) //secondary key
        {
        }
        // The following key isn't allowed because it contains fields from the base table and the table extension
        //key(ExtKey3; MyBaseField1, MyExtField2)
        //{
        //}
    }
}
```

>[!attention] Key Limitations in Table Extensions

- **Business Central 2020 release wave 2 and earlier**: Keys can only include fields from the table extension object.
- **Business Central 2021 release wave 1 and later**: Keys can include fields from either the base table object or table extension object, but not both in a single key.

>[!bug] Schema Synchronization Restrictions

- Don't delete primary keys.
- Don't modify primary key fields or their order.
- Don't change properties of existing primary keys.
- Don't add more unique or clustered keys.
- Don't add keys that include fields from both the base table and the table extension.

#### Tags
#BusinessCentral #TableExtension #IndexTuning #Performance #SchemaSynchronization