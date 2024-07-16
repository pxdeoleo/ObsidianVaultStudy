> [!summary] 
> Microsoft Dynamics 365 [[Business Central]] defines access through [[Entitlements and Permissions]], now transitioned from database data to AL code, improving security, traceability, and support.
>
#### Definitions
- **Entitlements**: Objects customers can use based on their license or [[Microsoft Entra]] ID role.
- **Permissions**: Objects assigned by an administrator or partner.

> [!info] New Object Types
- **EntitlementObject**
- **PermissionSet**
- **PermissionSetExtension**

> [!info] Transition to Code
> Permissions and entitlements, previously database data, are now AL language objects in Visual Studio Code. This enhances security, traceability, and support through DevOps practices.

> [!info] Advantages
- **Hotfix Application**: Similar to app updates, entitlements and permissions can now receive hotfixes, improving support agility and customer satisfaction.
- **Source Control**: Leverages Visual Studio Code and GitHub for designing and tracking changes.

> [!attention] Security and Audit
> Treat sensitive data like code to mitigate security and audit risks, adhering to DevOps principles.

> [!tip] Future Monetization
> New AL objects will enable ISVs to define app capabilities for customers purchasing licenses through Microsoft [[AppSource]].

#### Tags
#MicrosoftDynamics365 #BusinessCentral #Entitlements #Permissions #ALLanguage #DevOps #AppSource #ISV