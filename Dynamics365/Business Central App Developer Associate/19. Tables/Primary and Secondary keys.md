>[!summary]
Keys are essential in [[Table extensions|tables]] for making records unique and optimizing database performance. In AL (Application Language), keys are sequences of one or more field IDs from a table. They can be primary or secondary.

#### Definitions
- **Primary Key**: Uniquely identifies each record in a table; only one primary key per table; defined on table objects.
- **Secondary Key**: Creates indexes in SQL, defined on both table objects and table extension objects; multiple secondary keys are allowed.

>[!info] Primary Keys
- Uniquely identifies records.
- Defined on table objects only.
- First key defined in a table object is the primary key.
- Ensures logical order and uniqueness.
- Composed of up to 16 fields.
- Example: Sales Header table uses Document Type and No. fields.

>[!info] Secondary Keys
- Create SQL indexes, improving search performance.
- Defined on table objects and table extension objects.
- Can include fields from both base table and extension objects.
- Optional but beneficial for performance.
- Up to 40 keys per table; each can have a maximum of 20 fields.
- Example: Customer table can have secondary keys on Name, Address, and City.

>[!tip] Defining Secondary Keys
- Use the `Unique` property to create unique constraints.
- Use `IncludedFields` for non-key fields to improve query performance.
- Consider non-clustered columnstore indexes for large tables to improve analytics performance.

>[!info] Unique Secondary Keys
- Ensures records don't have identical field values.
- Multiple unique secondary keys can be defined on a table.

>[!info] Non-Clustered Columnstore Keys
- Improve query performance on large tables.
- Uses column-based data storage for better performance and compression.

>[!info] Performance Considerations
- Indexes speed up data retrieval but can impact update performance.
- SQL Server's Query optimizer helps identify columns for indexing.
- Use `sys.dm_db_missing_index_details` for missing index suggestions.

#### Limitations and Restrictions
- **Table Extension Objects**:
  - In BC 2020 Wave 2 and earlier: Keys can only include fields from the extension object.
  - In BC 2021 Wave 1 and later: Keys can include fields from both base and extension objects, but not mixed in a single key.
- **Key Modifications**:
  - Don't delete or change primary keys.
  - Avoid adding/removing primary key fields or changing their order.
  - Limit adding unique and clustered keys.
  - Avoid keys that are fields of the base table.

#### Tags
#keys #dynamics365 #businesscentral #database #performance