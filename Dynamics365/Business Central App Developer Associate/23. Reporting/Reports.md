>[!summary]
In Microsoft Dynamics 365 Business Central, a report specifies how data is collected, presented, or printed when the report is run. It consists of various components like properties, triggers, and layouts, and follows specific tasks for establishment.

#### Definitions
- **Report Object**: Specifies data collection, presentation, and print formatting in Business Central.
- **Property**: An attribute of an object/component specifying its behavior and visibility.
- **Trigger**: User-definable AL functions run by predefined events in a report.

>[!info] Report Components

- **Properties**: Attributes defining the behavior of report components.
- **Triggers**: Events causing specific functions to run. Categories include Report, Data item, and Request page triggers.
- **Controls**: UI elements within the report.
- **Data Items**: Sources of data for the report.
- **Columns**: Data fields presented in the report.
- **Request Page**: User interface for specifying report parameters.
- **Labels**: Text elements used in the report.
- **Layout(s)**: Design and arrangement of report elements.

>[!info] Establishing a Report

Developers complete the following tasks to establish a report object:
1. **Assign Report Name and ID Number**
2. **Specify Data Items**
3. **Design Report Layout**

>[!example] Report Triggers

Examples of report triggers include:
- **OnPreReport**: Executes statements before the report runs.
- **OnPostReport**: Executes statements just before the report run completes.

#### Tags
#MicrosoftDynamics365 #BusinessCentral #Reports #ALProgramming #ReportObject