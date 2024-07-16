> [!summary] 
> The visual layout determines the content and format of a report when viewed and printed. Reports must have a layout, and there are three types: RDL, Word, and Excel layouts.

#### Definitions
- **Report Layout**: Visual arrangement of data items and columns, specifying general format like text font and size for reports in Dynamics 365 Business Central.

> [!info] Report Layout Types

- **RDL Report Layouts**: Created using Microsoft Report Builder or SQL Server Reporting Services Report Builder. RDL layouts can slow performance with document reports due to user interface actions. They are not trusted from a service perspective and run in a sandbox app domain.
- **Word Report Layouts**: Created using Word documents with a custom XML part representing the report dataset. Recommended for document reports as they are not affected by security constraints like RDL layouts.
- **Excel Report Layouts**: Based on Excel documents (.xlsx) and utilize Excel's features like sliders, diagrams, charts, pivot tables, and PowerQuery for designing reports.

> [!tip] Extending Reports

- Existing reports can be extended to add new layouts.

#### Tags
#reportlayout #dynamics365 #rdl #wordlayout #excellayout #businesscentral