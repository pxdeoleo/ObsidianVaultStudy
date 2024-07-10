>[!summary]  
Organizations running on-premises workloads can migrate to Business Central online to leverage cloud benefits like Machine Learning, Power BI, and Power Automate. Migration requires SQL Server 2016+ with a database compatibility level of 130 or higher.

#### Definitions
- **Business Central Online**: Cloud version of Microsoft's business management solution.
- **Migration tools**: Built-in tools provided by Microsoft for data migration to Business Central online.

>[!info] Supported Products for Migration

Currently supported products for migration to Business Central online:

- **Dynamics GP 2015+**
- **Business Central on-premises**
    - Versions 14 to 19
    - Current version

To migrate from Dynamics NAV, upgrade to Business Central on-premises first.

>[!info] Prerequisites for Migration

Key prerequisites for migrating data:

- **Business Central Online Tenant**: Customer must have one.
- **Administrator Access**: Migration must be run by an administrator of the Microsoft 365 tenant and Business Central online.
- **Supported Migration Path**: Ensure the on-premises solution is supported.
- **Database Readiness**:
    - SQL Server 2016 or later
    - Compatibility level 130+
    - Update statistics and reorganize indexes
- **SUPER Permissions**: At least one user must have these in the target company.

>[!info] Considerations

Considerations for a smooth migration:

- Reduce the amount of data to migrate.
- Avoid scheduling conflicts with Business Central online updates.
- Install the necessary migration apps in Business Central.

>[!example] Installing Migration Apps

1. **Open Environment**: In the Business Central admin center, select the target environment and choose Apps.
2. **Install Updates**: Ensure the following apps are updated:
    - **Intelligent Cloud Base**
    - **Business Central Intelligent Cloud**
    - **Business Central Cloud Migration – Previous Release**
    - **Business Central Cloud Migration – Previous Release (region-specific)**
    - **Dynamics GP Intelligent Cloud**
    - **Dynamics GP History SmartLists**

Install the Intelligent Cloud Base extension first, followed by product-specific extensions.

>[!tip] Data Management

- Keep Business Central online storage under 80 GB.
- Ideally, migrate data in chunks less than 30 GB.
- For very large data migrations, run assisted setup to create a pipeline and contact Support for limitations adjustment.

>[!attention] Production Environment Warning

Avoid setting up cloud migration in a production environment already in use to prevent data overwrites. Even targeting a different company within the environment carries a risk of overwriting shared data.