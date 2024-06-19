**1. Core Architecture:**

- **Model-Driven Structure:** Core and major functionalities are divided into various models.
- **Element-Level Dependency:** Defines interactions among models to ensure a robust architecture.

**2. Platform Models:**

- **Categories:** Application platform, Application foundation, Test essentials.
- **Application Platform Functions:**
    - **Runtime and Data Access:** Core communication with the kernel.
    - **Workflow and Services:** Supports standard and custom workflows; integrates SOAP and JSON endpoints for custom services.
    - **Client and Presentation:** Manages user interactions through various devices with a user-friendly interface.
    - **SSRS Reporting:** Utilizes SQL Server Reporting Services for standard and custom reports.

**3. Application Foundation:**

- **Organization Structure:** Includes legal entities, operating units, and teams.
- **[[Number Sequence]]:** Generates unique identifiers.
- **[[Global Address Book]]:** Manages contact information for internal and external interactions.
- **Source Document:** Supports functionalities like accounting distributions and journal entries.

**4. Test Essentials:**

- **Testing Framework:** Provides FormAdaptors for testing form functionalities.
- **[[Task Recorder]] Integration:** Generates test code from Task Recorder XML files.

**5. Application-Specific Models:**

- **Examples:** Application suite, Ledger, Retail, Case management.
- **Application Suite:** Sits atop the Application foundation; contains key components like Supply Chain Management, Human Resources, Finance.
- **Other Models:** Cover specific functionalities like Currency, Directory, Contacts.

**6. Dynamics 365 Integration:**

- **Components:** Sales, Marketing, Service, Finance, Commerce, Supply Chain Management.
- **Focus:** Latter three are primary for finance and operations apps.