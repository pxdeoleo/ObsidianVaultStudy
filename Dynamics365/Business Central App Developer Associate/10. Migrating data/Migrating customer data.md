> [!summary] Migrating customer data to [[Business Central]] can be accomplished using built-in migration tools, RapidStart Services, or configuration packages. These methods help move data from various sources into Business Central online or on-premises environments.

#### Definitions

- **Business Central Online**: The cloud-based version of Business Central.
- **Business Central On-Premises**: The locally installed version of Business Central.
- **RapidStart Services**: A tool for configuration and data migration in Business Central.
- **Configuration Package**: A method for migrating data using Excel or .rapidstart files, often used when direct migration tools are not available.

> [!info] Migration Methods

- **Built-in Migration Tools**: Use these to migrate data from supported product versions directly to Business Central online.
- **Excel or RapidStart Services**: [[Migrate data to Business Central]] on-premises, then switch to the cloud if needed.
- **Configuration Package Approach**: Import data using Excel or .rapidstart files from unsupported products or custom sources.

> [!example] Configuration Package Approach

1. **Export Data to Excel**: From the Configuration Packages page, export the data to ensure it matches Business Central's structure.
2. **Map Tables and Fields**: On the Configuration Package page, define mappings for tables and fields to align data structures.
3. **Handle Relations**: Business Central processes mappings based on table relations:
    - Direct field mapping is prioritized.
    - If a field is related to another table, mappings for the primary key in the related table are used.
    - Conflicts are resolved by giving priority to direct field mappings over related table mappings.

> [!tip] Using Configuration Worksheet and Package Pages

- **Import Data**: You can import data from Excel or .rapidstart files from both the Configuration Worksheet and Configuration Package pages.
- **Mapping in Configuration Package Page**: Define and manage mappings to align data structures from source to destination.

> [!example] Steps for Migrating Data

1. **Prepare Data**: Ensure the data is in the correct format by exporting from the Configuration Packages page.
2. **Define Mappings**: Map tables and fields to match the Business Central data structure.
3. **Import Data**: Use the Configuration Worksheet or Configuration Package pages to import data from Excel or .rapidstart files.
4. **Verify Data**: Check the imported data to ensure it aligns correctly within Business Central.