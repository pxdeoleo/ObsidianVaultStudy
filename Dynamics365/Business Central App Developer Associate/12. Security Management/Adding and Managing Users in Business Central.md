>[!summary]  
Once a [[Business Central]] instance and company are set up, users can be added from Microsoft 365. Administrators can manage user permissions through security groups or individual assignments.

#### Definitions
- **Microsoft 365 Admin Center**: Portal for creating and managing users in Microsoft 365.
- **User Card**: A feature in Business Central that provides detailed information about users, their permissions, and group memberships.

>[!info] Adding Users in Microsoft 365

Steps to add a user in Microsoft 365:

1. **Open Admin Center**: Navigate to Users > Active Users > Add a User.
2. **Fill in Details**: Enter name, username, domain, and password settings.
3. **Assign License**: Select location and appropriate license (Dynamics 365 Business Central for IWs).
4. **Optional Settings**: Set roles and additional profile information.
5. **Review and Finish**: Review settings and finalize user creation.

>[!example] Adding Users in Business Central

1. **Search for Users**: Select the search icon, enter "Users," and choose the related link.
2. **Get Users from Microsoft 365**: Use the Get Users from Microsoft 365 action to import new users.
3. **User Information**: Access the user card from the Users list to view detailed user information.

>[!info] User Card Features

- **State Field**: Enable or disable users to control their access to Business Central.
- **Permissions**: View and assign user permission sets and group memberships.
- **Microsoft 365 Authentication**: Check if the user was created from Microsoft 365.
- **Company Access**: See which companies the user has access to and their permissions.

>[!tip] Managing Permissions

- **Assign Permission Sets**: Define access to database objects and UI elements.
- **User Groups**: Use groups to assign the same permission sets to multiple users for easier management.

>[!attention] User Activation

Users must be enabled in the State field to work within Business Central. Disabling a user prevents them from connecting to the application but keeps their record in the Users list.