>[!summary]  
To manage cloud migration from Business Central online while keeping the on-premises solution operational until migration completion, avoid setting up cloud migration in a production environment actively used for business. Migration will overwrite existing data in Business Central online with on-premises data.

#### Definitions
- **Cloud Migration Setup**: An assisted setup wizard in Business Central online for data migration.
- **Azure Data Lake**: A storage service used for historical data from Dynamics GP during migration.

>[!info] Key Considerations

- **Existing Data Overwrite**: Migration process overwrites data in Business Central online with on-premises data.
- **Configuration Caution**: Do not configure the connection if you want to preserve existing data in Business Central online.

>[!tip] Exception Scenario

Only migrate multiple times without overwriting data if using the current version of Business Central on-premises.

>[!info] SQL Server Procedures

Migrating from Business Central on-premises adds several stored procedures to the SQL Server instance, necessary for moving data to the Azure SQL server associated with the Business Central tenant.

>[!example] Main Steps in Migration Process

1. **Target Environment**: Ensure it has a paid subscription.
2. **Data Determination**:
    - **Business Central on-premises**: Select companies and determine the number of migration runs.
    - **Dynamics GP**: Use migration to move historical data to Azure Data Lake.
    - **Dynamics NAV**: Upgrade to Business Central on-premises first, then migrate.
3. **Migrate Data**: Use the Cloud Migration Setup assisted setup wizard in Business Central online.
4. **Test Migration**: Verify the migration results.
5. **Setup Configurations**: Establish users, permissions, and other settings in Business Central online.
6. **Switch Over**: Cease using the on-premises solution, turn off migration, and direct users to Business Central online for daily operations.

>[!attention] Production Environment Warning

Do not set up cloud migration for an actively used production environment to prevent overwriting necessary business data.