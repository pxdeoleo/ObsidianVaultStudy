>[!summary]
>Adding data sources to forms in Dynamics 365 Finance and Operations apps is a critical step in form development, enabling the display and manipulation of data within the user interface.

#### Definitions
- **Data Source**: A table or query that provides the underlying data for forms in the application.

>[!info] Adding Data Sources to Forms

Data sources are crucial for populating forms with data from the database. You can add data sources to your form in Visual Studio by dragging tables or queries from the Application Object Tree (AOT) or from within your project.

>[!bug] Common Pitfalls in Data Source Configuration

Incorrect data source configuration can lead to performance issues, data inconsistency, and errors in form functionality.

>[!info] Steps to Add a Data Source from AOT

1. Open your form in the Form Designer within Visual Studio.
2. Navigate to **View > Application Explorer** to open the Application Explorer window.
3. In Application Explorer, expand the **Data Model** node and then the **Tables** or **Table Extensions** node.
4. Drag the desired table from the Application Explorer to the **Data Sources** node in the Form Designer.

>[!tip] Best Practices for Data Source Selection

- Choose tables that directly relate to the form’s purpose to minimize unnecessary data processing.
- Use table extensions to customize data sources without modifying original tables.

>[!attention] Alternative Method to Add Data Source

If you prefer not to drag and drop, you can manually add a data source:
1. Right-click the **Data Sources** node in the Form Designer and select **New Data Source**.
2. In the Properties window, set the **Table** property by selecting the desired table from a drop-down list that includes all available tables and table extensions.

>[!example] Example of Adding a Data Source

To illustrate, if you're developing a form to manage customer information:
1. Drag the **CustTable** from the Application Explorer to the form’s **Data Sources** node.
2. Alternatively, add a new data source and select **CustTable** from the Table property in the Properties window.

This approach ensures that the form will display and interact with customer data effectively.

>[!info] Finalizing and Testing

After adding data sources, ensure the form layout and data bindings are correctly set up. Test the form to confirm that data loads correctly and that all functionalities such as search, filter, and edit are working as expected. Regularly updating and testing form designs are crucial for maintaining the effectiveness and usability of the application interfaces.