> [!summary] 
> The Environments tab of the [[Business Central]] administration center provides tools to manage production and sandbox environments, update schedules, and environment capacity. It is essential for managing Business Central's deployments and configurations.

#### Definitions

- **Environments Tab**: Allows viewing and managing Business Central production and sandbox environments.
- **Production Environment**: A live environment for business operations.
- **Sandbox Environment**: A non-production instance for testing, learning, and development.

> [!info] Starting Environment Quota

- Each new Business Central customer with a Premium or Essential subscription gets:
    - 1 production environment
    - 3 sandbox environments
- Extra production environments can be purchased, each including 3 sandbox environments and 4 GB additional database capacity.

> [!info] Environment Creation

- Environments can be created in any region where Business Central is available.
- Administrators can create environments through the Business Central admin center.

> [!example] Create Production Environment

1. Go to Environments tab in Business Central admin center.
2. Select New action.
3. Choose Production in the Type drop-down list.
4. Select country/region.
5. Click Create.

> [!example] Create Sandbox Environment

1. Go to Environments tab in Business Central admin center.
2. Select New action.
3. Name the environment.
4. Choose Sandbox in the Type drop-down list.
5. Optionally, choose to copy another environment.
6. Select country/region and application version.
7. Click Create.

> [!info] Sandbox from Production

- Create a sandbox environment from within a production environment for safe testing without affecting production data.
- Precautions include stopping job queues and blocking outbound HTTP calls by default.

> [!example] Copy Environment

1. In the Business Central admin center, select Environments.
2. Select the environment to copy.
3. Click Copy action.
4. Specify environment type and name.
5. Click Create.

> [!attention] Environment Precautions

- Job queues stopped.
- Base application integration settings cleared.
- Outbound HTTP calls blocked by default.

> [!info] Deleting Sandbox Environment

- Choose the environment on the Environments tab.
- Select Delete.
- Environments are soft-deleted for 7 days and can be restored without Microsoft support.

> [!info] Restoring Environment

- Azure SQL Database backups are used with a 30-day retention period.
- Restore within the same version and region.
- Specific permissions required: D365 BACKUP/RESTORE.

> [!example] Restore Environment

1. Go to Environments in admin center.
2. Select the environment.
3. Click Restore.
4. Specify date/time for restore.
5. Name the restored environment.
6. Click Restore.

> [!info] Transferring Environments

- Self-service transfer between [[Microsoft Entra]] tenants.
- Requires admin approval from both source and target tenants.

> [!info] Managing Access

- Assign Microsoft Entra ID groups to environments.
- Only group members can access the environment.

> [!example] Set Update Window

1. In Environments tab, select the environment.
2. Click Set update window.
3. Specify start and end time.
4. Click Save.

> [!example] Schedule Major Update

1. In Environments tab, select the environment.
2. Click Schedule Update.
3. Select desired update date.
4. Click Schedule Update.

> [!info] Managing Apps

- Updates for apps available in the admin center.
- Ensure updates are tested in sandbox environments before applying to production.

> [!info] Viewing Database Locks

- Search for Database Locks to view a snapshot of current database locks.

> [!info] Viewing Table Information

- Search for Table Information to see data distribution across tables.

> [!example] Manage Sessions

1. In admin center, select Manage Sessions.
2. Use Show session details for more information.

> [!info] Manage Capacity

- View and manage storage capacity in the Capacity section of the admin center.
- Option to purchase additional capacity if needed.

> [!example] Data Archive Extension

1. Pre-installed for archiving data via date compression.
2. Accessible from Extension Management.
3. Archives stored in Tenant Media table.

> [!info] Running Data Compression

- Use Data Administration to set up data compression for various data types.
- Archived data stored separately from the main database to save space.