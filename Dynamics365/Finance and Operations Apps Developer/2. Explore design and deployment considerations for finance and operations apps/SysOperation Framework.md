SysOperation Framework replaces [[RunBase Framework]], and provides more extensiblity.
Both support:
- Parameters
- Dialog UI
- Batch servers
- Running operations interactively
For Finance an Operations, **it is recommended** to use SysOperation instead of RunBase.
SysOperation should be used when a job should process or calculate something.

Consists of:
- [[Data contract class]]
- [[Controller class]]
- [[Service class]]
- [[UI Builder class]]
### Implement the SysExtensionSerializer
- Add fields to a table.
- The **SysExtensionSerializerMap** and **SysExtensionSerializerExtensionMap** maps make the create, read, update, and delete (CRUD) operations automated to the custom table.

Good practice: Create a new table and add a FK to the original table to extend it.
	When trying to add more than 10 fields to a table extension, the compiler will throw this best practice error.
	
Creating a new table for the new fields:
![[new_table_new_fields.png]]

**SysExtensionSerializerMap** automatically updates the originally referenced table.