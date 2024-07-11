>[!summary]  
Permission sets in [[Business Central]] define user access to database objects and UI elements. Administrators manage permissions by creating, modifying, and assigning permission sets to users or groups.

#### Definitions
- **Permission Set**: A collection of permissions for specific database objects in Business Central.
- **User Groups**: Collections of users to streamline permission management.
- **Security Groups**: Microsoft 365/Azure-based groups for managing permissions across [[Dynamics 365 applications]].

>[!info] Assigning Permission Sets

1. **User Card Page**: See and assign permission sets to users.
2. **Effective Permissions Page**: View permissions a user has and their sources.

>[!example] Creating or Modifying Permission Sets

1. **Navigate to Permission Sets**: Use the search icon to find the Permission Sets page.
2. **Select a Permission Set**: Choose the Permissions action to view and modify.
3. **Set Permissions**: Define Read, Insert, Modify, Delete, and Execute permissions as Yes, Indirect, or Blank.

>[!tip] Indirect Permissions

Indirect permissions allow a user to perform actions on an object through another related object. For example, a user with indirect permission for the Sales Line table can modify it through the Sales-Post codeunit but not directly.

>[!info] Record-Level Security

- **Security Filters**: Limit user access to specific records within a table.

>[!example] Recording Actions for Permission Sets

1. **Start Recording**: On the Permission Sets page, select the New action, name the set, and start recording.
2. **Perform Actions**: Navigate and perform tasks in Business Central.
3. **Stop Recording**: Finish and save the recorded permissions to the new permission set.

>[!info] Assigning Permissions to Users

1. **User Card**: Define permission sets directly on a user’s user card.
2. **Permission Set by User Page**: Select permission sets for users or user groups.

>[!info] Copying Permission Sets

1. **Select a Permission Set**: Use the Copy Permission Set action on the Permission Sets page.
2. **Define Copy Method**: Choose between Copy by reference, Flat permission copy, or Clone.

>[!example] Customizing Permissions by License

1. **Navigate to License Configuration**: Search for and select License Configuration.
2. **Select License**: Choose the license to customize and configure permissions.

>[!tip] User Email Policies

- **Email View Policies**: Control which emails users can view in the Email Outbox and [[Sent Emails]] pages.

>[!info] Effective Permissions

- **View Permissions**: Users can view their own permissions; administrators can view permissions of others with SECURITY or SUPER permissions.
- **Permission Sources**: Effective Permissions page shows the source of each permission and applied security filters.