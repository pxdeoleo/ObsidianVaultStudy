>[!summary]
>Tables in Dynamics 365 Finance and Operations apps are fundamental structures that store and organize data for user interfaces, such as forms and reports. They can be customized or extended to fit specific business needs.

#### Definitions
- **Table**: A database structure that contains rows (records) and columns (fields) used to store data.
- **Metadata**: Data that describes other data, like table settings or configurations.

>[!info] Table Components

Tables consist of various components that enhance their functionality in the application:
- **Fields**: Individual data items within a table, often defined by extended data types (EDTs) or base enumerations.
- **Field Groups**: Logical groupings of fields that simplify form and report design.
- **Indexes**: Structures that improve data retrieval speed.
- **Relations**: Links between tables that define how data in related tables is interconnected.
- **Delete Actions**: Configurations that determine the behavior when associated data is deleted.

>[!bug] Common Customization Mistakes

When modifying tables, it’s crucial to avoid duplicating existing extended data types or improperly setting table relations, which can lead to data integrity issues.

>[!info] Creating and Modifying Tables

To add a new table to a project:
1. In Solution Explorer, right-click the project and select Add > New Item.
2. Choose Table from the options and use the Table Designer to define fields, indexes, and other components.

>[!tip] Effective Use of Field Groups

Utilize field groups to organize fields in a way that reflects their usage in forms and reports, ensuring consistency and ease of maintenance.

>[!attention] Extension vs. Modification

Prefer creating extensions to tables rather than modifying existing tables directly to maintain upgrade compatibility and ease of application updates.

>[!example] Practical Table Setup

1. **Add Fields**: Drag fields from the Application Explorer or directly create them in the Table Designer.
2. **Configure Indexes**: Set up indexes for fields that are frequently queried to improve performance.
3. **Define Relations**: Establish relationships with other tables to ensure data consistency and integrity.
4. **Customize Field Groups**: Group related fields together to reflect how they are used in user interfaces.

>[!info] Integrating Table Changes

Once tables are configured, ensure they are properly integrated into the application, with appropriate security and access controls in place. This allows for seamless operation and user interaction with the newly customized or extended data structures.