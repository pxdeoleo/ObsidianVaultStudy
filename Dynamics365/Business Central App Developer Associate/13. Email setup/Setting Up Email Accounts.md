>[!summary]  
Business Central supports email accounts through various extensions, enabling connections to Microsoft Exchange Online, Google Gmail, and other providers using SMTP. Setting up email accounts involves specifying account details and configuration options.

#### Definitions
- **Email Extensions**: Extensions enabling email account connections in Business Central.
- **Microsoft 365**: Sends email from a shared Exchange Online mailbox.
- **Current User**: Sends email from the account used to sign in to Business Central.
- **SMTP**: Uses SMTP protocol to send emails through an SMTP mail server.

>[!info] Available Email Extensions

- **Microsoft 365**:
  - Sends emails from a shared mailbox (e.g., sales@cronus.com).
  - Requires setting up a shared mailbox in the Microsoft 365 admin center.

- **Current User**:
  - Sends emails from individual accounts used to sign in to Business Central.
  - Requires valid Exchange Online licenses.

- **SMTP**:
  - Allows communications through your SMTP mail server.
  - Configurable with various authentication methods.

>[!example] Setting Up an Email Account

1. **Open Assisted Setup**:
   - Select the search icon, enter "Set Up Email," and select the related link.

2. **Select Email Type**:
   - Choose between Microsoft 365, Current User, or SMTP.

3. **Configure Microsoft 365 Account**:
   - Enter Account Name and Email Address.

4. **Configure Current User Account**:
   - Automatically uses sign-in account settings.
   - Option to set as default.

5. **Configure SMTP Account**:
   - Enter details like Account Name, Sender Name, Email Address, Server URL, Server Port, Authentication, User Name, and Password.
   - Select Secure Connection if needed.

6. **Complete Setup**:
   - Follow the wizard steps to finish and close the setup.

>[!tip] Default Email Account

- **Requirement**: A default email account must be set, even if only one account is added. This account will be used for all email scenarios not assigned to a specific account.

>[!attention] Using SMTP Connector Extension

- **Legacy SMTP Setup**: Existing configurations can continue in parallel with the SMTP Connector extension.
- **Synchronization**: No synchronization between SMTP Connector and legacy settings. Update both if changes are made.

>[!info] Send As and Send on Behalf Capabilities

- **Send As**:
  - Change sender address on outbound messages using Microsoft Exchange.
  - Choose Specific User in the Sender Type field.

- **Send on Behalf**:
  - Amend sender address with "on behalf of" using Microsoft Exchange.
  - Choose Specific User in the Sender Type field.

- **Current User**:
  - Allows sending messages appearing from the user's sign-in account.
  - Similar to the Send As feature but uses the SMTP Connector setup.

#### Steps for Email Account Configuration

1. **Search for Set Up Email**: Use the search icon to find "Set Up Email" and select the related link.
2. **Select Email Type**: Choose Microsoft 365, Current User, or SMTP.
3. **Enter Account Details**: Fill in necessary fields based on selected email type.
4. **Complete Setup**: Follow the wizard and set the account as default if needed.

#### Key Points

- **Multiple Providers**: Extensions available for various email providers, including Microsoft Exchange Online and SMTP.
- **Configuration Options**: Detailed setup for each email type, ensuring proper email functionality.
- **Security and Authentication**: Options for secure connections and multiple authentication methods.