>[!summary]
Pages are essential for displaying and organizing data in Dynamics 365 [[Business Central]]. They serve as the primary interaction objects for users and can adapt to different devices such as phones, tablets, and web clients.

#### Definitions
- **Pages**: Core objects in [[Business Central]] used to display and organize data, adaptable to various devices.

>[!info] Page Composition

A page is defined in code and composed of:
- Controls
- Properties
- Actions
- Triggers

>[!info] Page Types

- **Role Center Page**: Not linked to a source table.
- **Blank Page**: Not linked to a source table.
- **Linked Pages**: Connected to a source table, displaying data from that table.

>[!tip] Device Independence

Pages are designed to be device-independent, allowing reuse across phone, tablet, and web clients.

>[!example] Creating and Configuring Pages

1. Define the page in code with necessary properties.
2. Add controls, actions, and triggers.
3. Configure properties and define actions for interactions with other pages.

>[!info] Controls and Actions

- **Controls**: Components on a page, each with properties, triggers, and actions.
- **Actions**: Operations that can be executed, often triggering other pages or processes.

>[!info] Page Description

Each page has a description similar to a table description, providing context and details about the page’s purpose and functionality.

#### Tags
#dynamics365 #businesscentral #pages #datadisplay #controls #properties #actions #triggers