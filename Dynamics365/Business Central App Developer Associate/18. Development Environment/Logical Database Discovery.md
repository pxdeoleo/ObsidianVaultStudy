> [!summary]
> Dynamics 365 [[Business Central]], a cloud application, is built on a database that stores data and objects used in the application. Developers can add and modify objects without building a new product version. Object types include tables, pages, reports, codeunits, queries, and XMLPorts. Extensions and object numbering conventions are essential for customization and development.

#### Database and Object Types
- **Database**: Stores data (e.g., customers, vendors) and objects (e.g., pages, tables).
- **Objects**: Tables, pages, reports, codeunits, queries, and XMLPorts.
  - **Table**: Describes data storage and retrieval.
  - **Page**: User interaction for viewing and modifying records.
  - **Report**: Printing and processing data.
  - **Codeunit**: Container for programming code.
  - **Query**: Efficient database querying.
  - **XMLPort**: Data import/export in XML or text format.
  - **Table Extension**: Extends existing table functionality.
  - **Page Extension**: Extends existing page functionality.

> [!info] Logical Database
- Different companies can be set up within the database.
- Data is company-specific; objects are not.
- Objects apply to all companies within the same database.

> [!info] Object Numbering Conventions
- **0-49,999**: Used by Microsoft for worldwide versions.
- **100,000-999,999**: Localized objects for specific regions.
- **50,000-99,999**: Tenant/customer customizations.
- **1,000,000-60,000,000**: Registered Solution Program (RSP) for ISV solutions.
- **70,000,000-74,999,999**: Extension development for [[AppSource]].

> [!info] Prefix and Suffix
- Ensures unique object names.
- Tags of at least three characters.
- Prevents naming conflicts when installing multiple extensions.
- Registration required for unique tags (email: d365val@microsoft.com).
- Use AppSourceCop tool to detect missing prefixes/suffixes.

#### General Rules for Prefix/Suffix
1. Must be at least 3 characters.
2. Object/field name must start or end with the prefix/suffix.
3. Registered tag wins in conflicts.
4. Set prefix/suffix at the top object level.
5. For base application or other apps, set prefix/suffix at the top object level and control/field/action level.

#### Tags
#BusinessCentral #Database #Objects #Extensions #Customization #Development #MicrosoftDynamics #ObjectNumbering #PrefixSuffix