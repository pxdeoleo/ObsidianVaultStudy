> [!summary] 
> Exporting databases from Business Central online environments to a local database involves creating an Azure storage account and generating a shared access signature (SAS) for secure file transfer.

#### Definitions

- **(.bacpac) file:** A file format for exporting databases, which can be imported into a local database.
- **Azure storage account:** A Microsoft Azure service that provides storage in the cloud, necessary for exporting (.bacpac) files.

> [!info] Azure Storage Account Setup

1. **Subscription:** Ensure you have a Microsoft Azure subscription.
2. **Access:** Use the Azure portal to create a general-purpose v2 storage account.
3. **Steps to Create Storage Account:**
    - Navigate to **All services** > **Storage Accounts** > **Add**.
    - Select subscription and create a new resource group.
    - Name the resource group and storage account (3-24 characters, lowercase letters, and numbers).
    - Select location and keep default values for other fields (Resource Manager, Standard, StorageV2, RA-GRS, Hot).
    - Review and create the storage account.

> [!info] Generate Shared Access Signature (SAS)

1. **Navigate:** On the Azure storage account, select **Shared access signature**.
2. **Configure:**
    - Allowed services: Select **Blob**.
    - Allowed resource types: Select **Container** and **Object**.
    - Allowed permissions: Select **Read**, **Write**, **Delete**, and **Create**.
    - Set start and end date/time (minimum 6 hours expiration).
    - Allowed protocols: Select **HTTPS only**.
3. **Generate SAS:** Select **Generate SAS and connection string** and copy the Blob service SAS URL.

> [!example] Create Export File from Business Central

1. In the Business Central administration center, go to the **Environments** list.
2. Select the environment name to view details.
3. On the action ribbon, select **Database** > **Create Database Export**.
4. Fill in the fields:
    - File Name: Specify or leave the default.
    - SAS URI: Paste the copied Blob service SAS URL.
    - Container Name: Enter the existing container name or a new one.
5. Start the export operation (may take minutes to hours). The (.bacpac) file is exported to the Azure storage account.

> [!info] Post-Export

- **Access File:** After export completion, access the file in the Azure storage account.
- **Export History:** View export activity in the Business Central administration center under **Database** > **View Export History**.