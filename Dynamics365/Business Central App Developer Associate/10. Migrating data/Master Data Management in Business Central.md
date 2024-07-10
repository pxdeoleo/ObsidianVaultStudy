> [!summary] 
> Master data management in Business Central allows synchronization of master data across multiple companies within the same environment. This feature ensures consistent data across all companies by subscribing to data from a source company and defining synchronization rules.

#### Definitions
- **Master Data Management**: A function in Business Central for synchronizing master data across several companies.
- **Source Company**: The company from which master data is synced.
- **Receiving Company**: The company that subscribes to and receives the master data from the source company.

> [!info] Capabilities of Master Data Management

- Subscribe a company to data from another company.
- Define tables and fields for synchronization.
- Filter table records for more control.
- Set up advanced synchronization couplings.
- Use job queues for immediate synchronization.
- Review synchronization logs in receiving companies.

> [!example] Enabling Master Data Management

1. Open the receiving company in Business Central.
2. Select the **Search for page** icon in the upper-right corner.
3. Enter **Master Data Management Setup** and select the related link.
4. In the **Source Company** field, select the company from which you want to sync master data.
5. Activate the **Enable Data Synchronization** field.

> [!tip] Managing Synchronization

- Access synchronization tables and logs from the Master Data Management Setup page.
- Initiate synchronizations as needed from the setup page.

#### Steps for Data Synchronization

1. **Setup in Receiving Company**: Configure the receiving company to subscribe to data from the source company.
2. **Define Synchronization Rules**: Select the tables and fields to synchronize, apply filters if necessary, and set up advanced couplings.
3. **Immediate Sync Using Job Queues**: Use job queues to automatically sync changes to the receiving companies.
4. **Review Logs**: Monitor and review synchronization logs in the receiving companies to ensure data consistency.