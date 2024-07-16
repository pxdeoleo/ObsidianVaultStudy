>[!summary]
[[Business Central]] employs entitlements and permissions to manage access to its functionalities. Entitlements define access based on the license or Microsoft Entra ID role, while permissions are assigned by administrators or partners through permission sets.

#### Definitions
- **Entitlements**: Access rights to Business Central objects as per the license or [[Microsoft Entra]] ID role.
- **Permissions**: Access rights assigned by administrators/partners via permission sets.
- **Permission Sets**: Logical groups of permissions assigned to users.

>[!info] Entitlements

Entitlements determine which Business Central objects a customer can use, based on their license or assigned Microsoft Entra ID role. They are only applicable in the online version of Business Central.

>[!info] Permissions

Permissions specify the objects users can access, assigned through permission sets by administrators or partners. These sets group permissions logically and can be assigned explicitly or via user groups.

#### Permission Sets Scope
- Predefined by Microsoft or software providers (ISV apps from [[AppSource]]).
- System permission sets are predefined and non-editable but can be copied for creating user-defined sets.
- User-defined permission sets can be created from scratch or as copies of system sets and are editable.

#### Creating Entitlements and Permission Sets in AL
Entitlements and permission sets are handled as AL objects in app development. These can be extended using:
- **EntitlementObject**
- **PermissionSet**
- **PermissionSetExtension**

#### Versions of Business Central
- Pre-2021 release wave 1: Permissions and entitlements were stored as data in application database tables, which included Entitlement, Entitlement Set, Membership Entitlement, Permission Set, and Permission.
- Post-2021 release wave 1: System permissions and entitlements are now defined in code using AL objects, enhancing maintenance, security, and audit capabilities.

#### Benefits of AL Object Transition
- Traceable and manageable changes through Visual Studio Code and source control systems.
- Ability to apply hotfixes efficiently.
- Facilitates monetization for ISVs by defining app capabilities via entitlements and permissions.

>[!example] Transition to AL Objects

For existing systems, permissions and entitlements previously stored as data should be transitioned to AL objects. User-defined permission sets and functionality remain stored as data in the tenant database.

#### Tags
#BusinessCentral #Entitlements #Permissions #ALObjects #AccessControl