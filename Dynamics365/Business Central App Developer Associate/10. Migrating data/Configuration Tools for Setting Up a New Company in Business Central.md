> [!summary] 
> Configuration tools in [[Business Central]] facilitate the setup and initialization of new companies by creating packages with setup data and master data tables. These tools enhance the efficiency and quality of implementations for Microsoft partners.

#### Definitions

- **Configuration Worksheet**: A tool for listing and organizing tables needed for company setup.
- **Configuration Packages**: Bundles of setup and data tables applied to new companies.
- **Configuration Questionnaires**: Forms for gathering setup data from users.
- **Configuration Templates**: Pre-defined settings for typical setup configurations.

> [!info] Uses of Configuration Tools

- To configure add-on solutions
- To prepare demos
- For mass deployment
- When switching from trial to production
- To configure subsidiaries

> [!example] Common Tasks for New Company Setup

- Create a chart of accounts
- Set up number series
- Define payment terms
- Sales and purchases setup

#### Required Tables for Configuration

- **Default Data Records**: e.g., country or region codes.
- **Default Setup**: e.g., source code setup.
- **Area Setup**: e.g., Sales & Receivables Setup.
- **Supplementary Setup**: e.g., posting groups, payment terms.
- **Data Migration**: Tables requiring data migration.
- **Opening Balances**: Tables for posting opening balances.

#### Configuration Worksheet Page Fields

- **Line Type**: Specifies type (Area, Group, Table).
- **Table ID**: ID of the table used for the line type.
- **Page ID and Page Name**: Primary page for viewing records.
- **No. of Records**: Number of database records.
- **Licensed Table and Licensed Page**: Indicates license status.
- **Reference**: Additional information or URL.
- **Promoted Table**: Signifies tables requiring more attention.
- **Responsible ID**: ID of the responsible Business Central user.
- **Status**: Status of the table (In progress, Completed, Ignored, Blocked).

#### Adding Tables to Configuration Worksheet

- **Get Tables Function**: Options include:
    - Include with Data Only
    - Include Related Tables
    - Include Dimension Tables
    - Include Licensed Table Only

#### Creating Configuration Packages

1. Select lines in the Configuration Worksheet.
2. Use the **Assign Package** function to create a new package.
3. Fields in **Config. Package Card** include:
    - Code and Package Name
    - Product Version
    - Language ID
    - Processing Order
    - Exclude Config. Tables

#### Modifying Configuration Packages

- Limit exported fields.
- Validate fields before applying.
- Determine processing order.
- Filter table data.
- Connect configuration templates.

#### Exporting and Applying Configuration Packages

- Export from default company as .rapidstart or .Excel file.
- Contents include:
    - Configuration worksheet
    - Configuration package card
    - Table data
    - Configuration questionnaires
    - Configuration templates

#### Example: Creating G/L Account Journal Lines

1. Search for **Create G/L account journal lines**.
2. Fill in the fields on the **Create G/L account journal lines** page.
3. Select **OK** to create lines for each account in the specified journal.