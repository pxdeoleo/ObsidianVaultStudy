
>[!summary]  
Manage permission sets for multiple users efficiently by setting up user groups and security groups in Business Central. User groups are Business Central-specific, while security groups are based on Microsoft 365 or Azure Active Directory and will eventually replace user groups.

#### Definitions
- **User Groups**: Collections of users within Business Central for easier permission management.
- **Security Groups**: Microsoft 365 or Azure Active Directory-based groups for managing permissions across multiple Dynamics 365 applications.

>[!info] Creating User Groups

1. **Search for User Groups**: Use the search icon, enter "User Groups," and choose the related link.
2. **Add Users to Group**: On the User Groups page, select the User Group Members action, then choose Add Users.

>[!example] Copying User Groups

1. **Search for User Groups**: Enter "User Groups" and select the related link.
2. **Copy User Group**: Select the user group to copy, choose the Copy User Group action, enter a name for the new group, and select OK.

>[!info] Managing User Groups

- **Assign Permission Sets**: Assign relevant permission sets to define access for user group members.
- **User Group Members**: Members must be added manually after creating or copying a user group.

>[!info] Creating Security Groups in Microsoft 365

1. **Add a Group**: In the Microsoft 365 admin center, go to Active teams & groups, select Add a group, choose Security type, and follow prompts to specify group details.
2. **Add Members**: Open the group and use the Add members tab to include users.

>[!example] Linking Security Groups in Business Central

1. **Search for Security Groups**: Use the search icon, enter "Security Groups," and choose the related link.
2. **Create New Group**: Select New, enter a name, and specify the Microsoft Entra ID security group name.
3. **Assign Permissions**: On the Security Groups page, select the group and use the Permissions action to assign permission sets.

>[!info] Permission Assignment

- **Individual Permissions**: Choose permission sets individually in the Permission Set field.
- **Multiple Permission Sets**: Use the Select Permission Set action to assign multiple sets.
- **FactBox Pane**: Shows the Permission Sets assigned to the group and members' permissions.

>[!attention] Migration to Security Groups

- **Convert User Groups**: Use the User Group Migration assisted setup guide to convert user groups to permission sets.
    - **Assign to User**: Directly assign permissions to users and remove group assignments.
    - **Convert to Permission Set**: Create new permission sets from user groups and assign to all group members.