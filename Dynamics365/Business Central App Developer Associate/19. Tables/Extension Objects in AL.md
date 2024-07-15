>[!summary]
With an extension object, you can add new fields, actions, layouts, and values to existing pages, reports, enumerations, and other base objects in AL (Application Language). From runtime 13.0, extension objects can coexist with their targets within the same app, enabling nondisruptive code refactoring and modular development.

#### Definitions
- **Extension Object**: An AL object that extends existing base objects (tables, pages, reports, enums, etc.) with additional functionalities.
- **Extensible Property**: A property (`Extensible = true;`) that allows an object to be extended, which is true by default for all objects.

#### Types of Extension Objects
- **Table Extension**: Adds fields to an existing table.
- **Page Extension**: Adds fields, actions, and layouts to an existing page.
- **Report Extension**: Adds data items, columns, request pages, and layouts to an existing report.
- **Enum Extension**: Adds new values to an existing enumeration.
- **Permission Set Extension**: Adds new permissions to an existing permission set.

>[!info] Runtime 13.0 Features

From runtime 13.0 onwards, extension objects can coexist with their targets within the same app, allowing for better separation of concerns and modular development. This means:
- Extension objects reside in the same app as the base object.
- They maintain separate metadata, requiring unique object IDs.
- [[Table extensions]] merge fields and keys into the base table in the database schema, eliminating the need for SQL joins at runtime.

#### Benefits
- **Non-disruptive Refactoring**: Allows dividing objects into modules based on functionality or preparing to move objects into separate apps.
- **Flexibility**: Supports multiple extensions for a single target within the same app.

#### Compiler Validations Introduced
- Base objects cannot reference members from extension objects.
- Extension objects can only reference members from other extension objects within the same app if the other extension object has a lower object ID.

#### Tags
#extensionobjects #AL #runtime13 #modulardesign #softwaredevelopment