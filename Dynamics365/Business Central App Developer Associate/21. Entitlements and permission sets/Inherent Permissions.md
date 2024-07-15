>[!summary]
The 2022 release wave 2 introduced enhanced inherent permissions for developers, allowing them to override entitlements and grant temporary permissions during code execution to simplify permission management and improve security.

#### Definitions
- **Inherent Permissions**: Temporary permissions granted during the execution of a specific method or event.
- **Entitlements**: Permissions derived from user-assigned licenses and roles.

>[!info] Previous Implementation
- Before 2022 wave 2, inherent permissions only allowed extending role permissions.
- Permissions could not exceed what entitlements allowed.
- Developers could not grant fewer permissions than entitlements or exceed them with AL code.

>[!info] New Capabilities in 2022 Wave 2
- Inherent permissions can now override entitlements.
- Permissions are granted temporarily during code execution and revoked after.
- Simplifies permission management by limiting long-term permissions and giving permissions to code processes instead.

>[!example] Usage Scenario
- A salesperson needs a report with critical information.
- A method fetches classified data for the report.
- Instead of managing long-term permissions for the salesperson, inherent permissions grant access temporarily to the method.

>[!code] Code Example
```al
[InherentPermissions(PermissionObjectType::Table, Database::Customer, 'r', InherentPermissionsScope::Both)]
Procedure GetCustomersLocation(): CustomerLocation
```
- The above code grants read permission to the method to fetch customer locations without exposing other data.

>[!info] Best Practices
- Use inherent permissions for small, dedicated procedures or system tasks.
- Avoid risking data exposure to users by limiting the scope of granted permissions.

>[!note] Restrictions
- Inherent permissions can only be used for objects within the same extension.
#### Tags
#inherentpermissions #release2022wave2 #permissions #security #ALcode