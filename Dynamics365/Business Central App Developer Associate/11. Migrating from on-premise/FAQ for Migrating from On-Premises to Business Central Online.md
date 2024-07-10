>[!summary]  
This unit addresses frequently asked questions about migrating from on-premises solutions to Business Central online. Key topics include supported products, migration limits, SQL connection requirements, and handling customizations and permissions.

#### Definitions
- **Azure Data Factory (ADF)**: Service facilitating data migration from on-premises solutions to Business Central online.
- **Self-Hosted Integration Runtime (SHIR)**: Local runtime managing communication between cloud services and on-premises data.

>[!info] Supported Products and Versions

- **Migration Tools**: Built-in tools for migrating data to Business Central online.
- **Supported Versions**:
    - **Dynamics GP**: 2015 and later
    - **Business Central On-Premises**: Versions 14 to 19 and the current version
    - **Dynamics NAV**: Upgrade to Business Central on-premises before migrating online

>[!info] Data Migration Process

- **ADF Pipeline**: A data pipeline is created in ADF to transfer data from on-premises to Business Central online.
- **SHIR Configuration**: Required for local SQL Server instances, managing secure communication without opening ports/firewalls.

>[!info] Migration Limits

- **Data Size**: Default limit is 80 GB. Reduce the number of companies migrated if exceeding this limit.
- **Adding Companies**: Use the Cloud Migration Management page in Business Central online to add more companies.

>[!info] SQL Connection String

- **Requirement**: The SQL connection string is encrypted and used by ADF to communicate with the SQL Server instance.
- **Finding Connection String**: Obtain from SQL Management Studio or Visual Studio with SQL Authenticated user credentials.

>[!info] Integration Runtime Name

- **Finding Name**: Use Microsoft Integration Runtime Manager found in the Windows system tray or by searching the program.

>[!attention] Customizations and Permissions

- **Data Migration**: Only tables available in both on-premises and online environments migrate. Customizations must be made into extensions.
- **Restricted Permissions**: Users are added to the Intelligent Cloud user group during migration. Permissions can be reassigned post-migration.

>[!info] Pausing Migration

- **Switch Off Connection**: Disables synchronization, making on-premises and online solutions independent.
- **Reassign Permissions**: If using Business Central online as the primary solution, assign read/write permissions to users.

>[!attention] User and Permission Replication

- **No Replication**: On-premises users and permissions do not replicate due to lack of Microsoft Entra ID configuration.
- **Manual Addition**: Add and grant permissions to users in Business Central online manually.

>[!info] Data Replication Direction

- **One-Way**: Data replicates from on-premises to Business Central online only. On-premises solution must be discontinued post-migration.

>[!tip] Extensions Management

- **Uninstallation**: Uninstall extensions that send data to external services to avoid duplicated calls. Test extensions in a sandbox tenant configured for the Business Central online environment.