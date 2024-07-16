>[!summary]
The report object in AL Language defines the data model or dataset of a report for Dynamics 365 Business Central. Reports structure and summarize information, displaying and printing documents like sales quotes and invoices. The report creation involves defining the data model and the visual layout.

#### Definitions
- **Report Object**: Defines the data model and dataset of a report in AL Language.
- **Dataset**: Determines the data extracted or calculated from the database tables.
- **Visual Layout**: Determines the content and format of a report when viewed or printed.

>[!info] Report Creation

Creating a report consists of two primary tasks:
1. **Create the underlying data model**: Defines which database tables and fields to pull data from.
2. **Define the visual layout**: Displays the data in a specified format when viewed or printed.

>[!info] Dataset

The report dataset is built by adding data items and columns. It determines the data extracted or calculated from the Microsoft Dynamics 365 Business Central database tables used in a report.

>[!info] Layout Types

There are three types of report layouts:
1. **RDL Layouts**: Defined in Visual Studio Report Designer or Microsoft SQL Server Reporting Services Report Builder.
2. **Word Layouts**: Created using Word and based on a custom XML part representing the report dataset.
3. **Excel Layouts**: Created in Excel, utilizing Excel features like sliders, diagrams, charts, pivot tables, and PowerQuery.

One report can contain multiple report layout definitions.

>[!tip] Modifying Existing Reports

To modify an existing report (e.g., adding new columns, modifying the request page, or adding a new layout), create a report extension instead of altering the original report.

#### Tags
#AL_Language #Dynamics365 #BusinessCentral #ReportDesign #ReportLayout #Dataset