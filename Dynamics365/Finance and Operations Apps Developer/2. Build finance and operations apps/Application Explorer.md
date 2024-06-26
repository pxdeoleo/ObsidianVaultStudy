>[!summary]
>The Application Explorer in Visual Studio for Dynamics 365 finance and operations apps provides two primary views, the model view and the classic view, to navigate and manage metadata effectively.

#### Definitions
- **Application Explorer**: A component of Visual Studio that displays the Application Object Tree (AOT) and allows developers to interact with various elements of Dynamics 365 applications.

>[!info] AOT Views

1. **Model View**: Organizes metadata by the model, facilitating the exploration of elements related to specific features of a model.
2. **Classic View**: Groups metadata by type, aiding in locating specific types of elements regardless of the model they belong to.

>[!bug] Understanding Metadata

Understanding the difference between metadata types is crucial for effective development and maintenance of finance and operations apps.

>[!info] Metadata Types

- **Extended Data Types (EDTs)**: Fundamental data types like Boolean, String, and Integer.
- **Enums**: Defined lists of values, such as days of the week, stored efficiently in the database.
- **Tables**: Structures that organize data into rows and columns.
- **Forms**: UI elements within finance and operations apps.
- **Data Entities**: Abstractions of tables for data operations and integrations.

>[!tip] Efficient Navigation

Use the model view to explore elements by model when working on model-specific features, or switch to the classic view when searching for specific types of elements.

>[!attention] Other AOT Elements

Beyond basic metadata, the Application Explorer includes:
- **Analytics**: For handling dimensions, measurements, and KPIs.
- **Label Files**: For multilingual support in UI and code.
- **Reports**: Must be published in SSRS before use.
- **Resources**: For storing media and web content.
- **Configuration**: For managing license codes and settings.
- **Security**: For configuring roles, duties, and access controls.
- **Services**: For custom service implementations.

>[!example] Using the AOT

To find a specific table:
1. Open the Application Explorer.
2. Choose the classic view to browse by element type.
3. Navigate to Tables, and use the search function if necessary.
4. Double-click on a table to open its structure.

>[!info] Searching and Refreshing the AOT

Use the search functionality to filter elements by typing the element type followed by a colon and the search term. If recent changes are not reflected, use the Refresh button to update the view. For a comprehensive search guide, utilize the search field suggestions in the Application Explorer.

By mastering the use of the Application Explorer's features, developers can enhance their productivity and accuracy in managing the vast array of elements within Dynamics 365 finance and operations apps.