>[!summary]  
Business Central provides tools to audit changes and monitor sensitive fields. The change log tracks modifications to data, and field monitoring notifies administrators of changes to critical data fields.

#### Definitions
- **Change Log**: Tracks direct modifications made by users to data in specified tables and fields.
- **Field Monitoring**: Monitors changes to sensitive data fields and sends notifications.

>[!info] Setting Up the Change Log

1. **Activate Change Log**:
    - Select the search icon, enter "Change Log Setup," and select the related link.
    - Choose Setup > Tables to specify which tables and fields to track.

2. **Log Options**:
    - For each table, choose Log Insertion, Log Modification, or Log Deletion.
    - Select "Some Fields" and use the AssistEdit action to specify fields.

3. **Track Important Fields**:
    - Focus on system fields like Created By and Created Date.
    - Avoid tracking all fields to reduce performance impact and database size.

4. **Viewing Changes**:
    - After activation, view changes on the Change Log Entries page, showing details like Date and Time, User ID, Table Caption, Field Caption, Old Value, and New Value.

5. **Deleting Entries**:
    - Use the Delete Change Log Entries page to set filters and delete old entries.

>[!example] Configuring the Change Log

1. **Open Change Log Setup**: Use the search icon to find "Change Log Setup" and select the related link.
2. **Specify Tables and Fields**: Choose Setup > Tables, and specify tables and fields to track.
3. **Select Tracking Type**: Choose Some Fields for critical fields and set them up using the AssistEdit action.

>[!info] Monitoring Sensitive Fields

1. **Run Setup Guide**:
    - Select the search icon, enter "assisted setup," and choose the related link.
    - Locate "Set up field monitoring" and start the wizard.

2. **Specify Fields and Notifications**:
    - Add fields based on their classification (sensitive, personal, company confidential).
    - Set up notification recipients and email accounts.

3. **Manage Monitoring**:
    - On the Monitored Fields Worksheet, add or remove fields to monitor, set or clear notifications, and access Field Monitoring Setup and Field Change Entries pages.

4. **Viewing Changes**:
    - Use Field Change Entries on the Monitored Fields Worksheet or search for "Monitored Field Log Entries" to view details of changes.

>[!example] Setting Up Field Monitoring

1. **Run Monitor Field Change Setup**: Use the search icon to find "assisted setup," and start the "Set up field monitoring" wizard.
2. **Add Fields and Recipients**: Specify fields to monitor and set up email notifications.
3. **Manage Settings**: On the Monitored Fields Worksheet, manage field monitoring and notifications.

>[!info] Retention Policies

1. **Set Up Retention Periods**:
    - Select the search icon, enter "retention policies," and choose the related link.
    - On the Retention Policies page, navigate to Retention Periods, create a new retention period, and specify the duration.

2. **Define Retention Policies**:
    - On the Retention Policies page, select New, enter the Table ID, select the retention period, and enable the policy.
    - Optionally, apply filters to specify which records to delete.

3. **Automatic and Manual Application**:
    - Retention policies can be applied automatically using a job queue entry or manually using the Apply Manually action.

4. **View Activity**:
    - Use the Retention Policy Log page to view entries related to the application of retention policies.

>[!example] Creating a Retention Policy

1. **Open Retention Policies**: Use the search icon to find "retention policies" and select the related link.
2. **Create Retention Period**: Navigate to Retention Periods, create a new period (e.g., 10 months), and specify the date formula.
3. **Define Policy**: On the Retention Policies page, select New, enter the Table ID, set the retention period, and enable the policy.