>[!summary]
>Finance and operations apps utilize a comprehensive security framework to manage user access to reports and data, ensuring secure and role-based data visibility.

#### Definitions
- Role-Based Security: A system where access to program elements is controlled by user roles that aggregate security permissions, privileges, and duties.

>[!info] Security Configuration

Users can manage and view security roles, along with their associated duties, privileges, and permissions, through the Security configuration page in the system administration module.

>[!bug] Security Misconfigurations

Improper configuration of security roles or data security policies can lead to unauthorized access or restricted access to critical data, impacting business operations.

>[!info] Hierarchical Security Model

The security model in finance and operations apps is structured hierarchically:
- **Permissions**: The basic elements that describe access to individual operations.
- **Privileges**: Collections of permissions, typically aligned with tasks.
- **Duties**: Collections of privileges that represent parts of a user's job.
- **Roles**: Aggregates of duties assigned to users based on their job functions.

>[!tip] Efficient Role Assignment

Assign roles based on user job functions and responsibilities to streamline access management and maintain operational integrity.

>[!attention] Data Security Frameworks

Utilize the [[Extensible Data Security (XDS)]] framework to restrict data access at the transactional level and the [[Table Permissions Framework]] for granular control at the table level.

>[!example] Configuring Data Access

1. Define security roles with appropriate privileges and duties.
2. Assign roles to users based on their need to access specific reports and data.
3. Configure data security policies using the XDS framework to limit transactional data access based on user or role.
4. Use the Table Permissions Framework to set Create, Read, Update, or Delete permissions on sensitive data tables like ManagerFinancialData.
5. Verify that the Application Object Server (AOS) enforces these permissions consistently across user requests.

>[!info] Protecting Sensitive Data

Implement role-based and data security measures comprehensively to ensure that sensitive financial data is accessible only to authorized users, enhancing data protection and compliance with business policies.