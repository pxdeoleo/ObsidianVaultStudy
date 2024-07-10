>[!summary]  
Data migration involves securely transferring data from on-premises SQL Server or Azure SQL to Business Central online using Azure Data Factory (ADF). It requires SQL permissions and tracks success and failures table by table.

#### Definitions
- **Azure Data Factory (ADF)**: Service used to migrate data between databases.
- **Self-Hosted Integration Runtime**: A service installed on-premises to facilitate data migration to the cloud.

>[!info] Migration Process

Key aspects of the migration process:

- **Initial Migration**: Takes the longest, transferring all data.
- **Subsequent Migrations**: Faster, only transferring changes since the last migration.
- **Schema Matching**: Tables fail to migrate if schemas don't match between cloud and on-premises.

>[!example] Main Steps in Migration Process

1. **Prepare Target Environment**: Ensure a paid subscription.
2. **Select Data to Migrate**:
    - Choose companies for Business Central on-premises.
    - Move historical data to Azure Data Lake for Dynamics GP.
    - Upgrade Dynamics NAV to Business Central on-premises first.
3. **Run Cloud Migration Setup**:
    - Run the Cloud Migration Setup wizard in the target company.
    - Sign in as an admin of Microsoft 365 and Business Central online.
    - Obtain approval from a licensed user with SUPER permissions if using a delegated admin.
    - Start migration from a non-target company like CRONUS to ensure user logout.
4. **Configure SQL Connection**:
    - Specify SQL Server or Azure SQL connection.
    - Provide SQL connection string.
    - Define or install Integration Runtime service.
5. **Initiate Migration**: Trigger manually or schedule.

>[!attention] Existing Data Overwrite

Migration overwrites Business Central online data with on-premises data. Avoid connecting if preserving existing data.

>[!info] Cloud Migration Management

Manage and monitor migration:

- **Manage Schedule**: Set migration schedule.
- **Run Migration Now**: Manually start migration.
- **Run Data Upgrade Now**: Upgrade data for version migration.
- **Refresh Status**: Update migration status.
- **Reset Cloud Data**: Clear cloud data and restart migration.
- **Get/Reset Runtime Service Key**: Secure runtime key management.
- **Disable Cloud Migration**: End migration and prevent overwriting.
- **Check for Updates**: Ensure up-to-date migration service.
- **Select Companies to Migrate**: Specify companies for migration.
- **Define User Mappings**: Map on-premises users to Microsoft 365 users.
- **Setup Checklist**: Complete migration setup.

>[!info] Permissions Management

During migration from Business Central on-premises:

- **Intelligent Cloud User Group**: Users without SUPER permissions are assigned read-only access.
- **SUPER Permissions**: Required for at least one user per company.
- **Custom Permissions**: Create from Intelligent Cloud permission set for further restrictions.

>[!info] Company Initialization

Post-migration, companies must be initialized before access:

- **Initialization Task**: Runs as a scheduled job.
- **Hybrid Companies List**: Manage initialization status.

>[!tip] Avoid Production Environment

Do not migrate in an active production environment to prevent data overwrite.

#### Additional Features

**Include/Exclude Tables**: Customize data migration:

- **Include Subset**: Reduce cloud environment complexity.
- **Include Additional Data**: Migrate non-default data like change logs.
- **Delta Sync**: Replicate only new/changed data.
- **Limitations**: System tables and on-premises scope tables cannot be changed.

To use, go to the Cloud Migration Setup page, select **Include/Exclude Tables**, and configure settings for each table.