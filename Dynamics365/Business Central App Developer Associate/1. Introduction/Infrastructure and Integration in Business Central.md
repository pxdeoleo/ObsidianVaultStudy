>[!summary]
>[[Business Central]] utilizes Internet Information Services (IIS), Service Tiers (NST), and databases (DB) to provide a robust web-based environment, supporting multi-tenant architecture and seamless integration with external applications through web services.

#### Definitions
- IIS: Internet Information Services, which hosts the Business Central Web Server instance for client access.
- NST: Business Central Service Tier, responsible for executing business logic.
- DB: Database where Business Central stores application and business data.

>[!info] Web Server and Service Tier Setup

Set up the IIS website to facilitate user access to Business Central via web clients and integrations with Microsoft Outlook and companion apps.

>[!bug] Integration Points

Carefully manage the integration of IIS, NST, and DB to ensure seamless data flow and service delivery without interruptions.

>[!info] Web Services in Business Central

Leverage SOAP and ODATA web services to expose Business Central functionalities to external systems, enhancing interoperability and data exchange.

>[!tip] Developing Connect Apps

Utilize the Business Central REST API to develop connect apps, allowing integration with various external applications using any programming language that supports REST.

>[!attention] Multi-tenant Architecture

Understand and utilize the multi-tenant architecture of Business Central, which stores each tenant's data separately but shares a common data schema across localizations.

>[!example] Authenticating Users with [[Microsoft Entra]] ID

Configure the Business Central server instance to use [[Microsoft Entra]] ID for user authentication, linking Business Central accounts with Microsoft 365 for unified access across applications.

>[!info] Administrative Capabilities

If you're a Business Central reselling partner, manage tenant settings through the Business Central Administration Center and Microsoft 365 administration tools, including scheduling upgrade windows for optimal performance and compliance.