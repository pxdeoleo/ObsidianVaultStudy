>[!summary] 
With Business Central, you're provided with a license to Microsoft Power Automate, enabling you to create and run automated workflows using Business Central data and other internal and external sources. Power Automate supports automated, scheduled, and instant flows, which can be triggered by various events or run on-demand from within Business Central.

#### Definitions
- **Power Automate**: A service for creating automated workflows between apps and services, enhancing efficiency by reducing manual tasks.
- **Business Central Connector**: A tool that allows Power Automate to connect to Business Central data.
- **Flows**: Automated workflows created in Power Automate, which can be triggered by events, scheduled, or run on demand.

>[!info] Flow Types
There are three types of flows in Power Automate:

1. **Automated**: Triggered by specific events like record creation, modification, or deletion.
2. **Scheduled**: Runs periodically at set dates and times.
3. **Instant**: Manually triggered by the user from within Business Central.

>[!example] Example Flows
- **Automated Flow**: A new sales invoice triggers an approval request flow, which sends notifications based on the approver's response.
- **Scheduled Flow**: A daily report generation at a specified time.
- **Instant Flow**: Blocking payments to a vendor and sending emails from the Vendors page.

>[!info] Integration with Business Central
- Users can create, manage, and run flows from within Business Central using the Automate group in the action bar.
- Flows can connect Business Central with other Microsoft and third-party services, such as Outlook, Teams, SharePoint, and more.

>[!tip] Creating and Managing Flows
- **Create a Flow**: Select Automate > Create a Flow from a list, card, or document page.
- **Manage Flows**: Select Automate > Manage Flows to handle existing flows.
- **Personalize Actions**: Use personalization or designer mode to move, promote, or hide Automate actions.

>[!attention] User Permissions
- By default, all users have access to Power Automate features but must agree to the privacy notice to activate them.
- Administrators can control access by assigning or removing the system permission Allow Action Automate (ID 9630) or using the AUTOMATE - EXEC permission set.
- Administrators can agree to the privacy terms on behalf of users, eliminating the need for individual agreement.

>[!info] Running Flows
- Flows can be run from most list, card, and document pages in Business Central.
- Select Automate from the action bar, choose a flow, fill in required fields, and run the flow.
- The first-time use requires agreeing to the privacy notice via the Get Started with Power Automate action.

>[!info] Power Automate Integration Setup
- The Automate item is available on most pages but can be hidden or restricted by an administrator.
- Users must agree to the privacy notice to enable Power Automate features.
- Administrators can manage user permissions and privacy settings to control access to Power Automate.