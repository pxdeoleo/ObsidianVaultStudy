>[!summary]
When developing an app in AL for Dynamics 365 [[Business Central]], you can handle entitlements and permission sets as objects, and you can extend existing permission sets. Object types include EntitlementObject, PermissionSet, and PermissionSetExtension.

### Definitions
- **EntitlementObject**: Defines what objects a customer can use based on their license or role.
- **PermissionSet**: Specifies permissions on objects.
- **PermissionSetExtension**: Extends permissions of an existing PermissionSet.

>[!info] Entitlement Object
- **Description**: Describes objects a customer is entitled to use according to their license or [[Microsoft Entra]] ID role.
- **Components**: Consists of PermissionSet objects.
- **Scope**: Only includes objects within the same app to ensure app boundaries.
- **Usage**: Only for online versions of Dynamics 365 Business Central.

>[!example] Example: Entitlement Object
```al
entitlement BC_Role_Delegated
{
    Type = Role;
    RoleType = Delegated;
    Id = '1a2aaaaa-3aa4-5aa6-789a-a1234567aaaa';
    ObjectEntitlements = "D365 BUS PREMIUM - BaseApp";
}
```
```al
entitlement BC_PerUserServicePlan
{
    Type = PerUserServicePlan;
    Id = '1a2aaaaa-3aa4-5aa6-789a-a1234567aaaa';
    ObjectEntitlements = "D365 BASIC";
}
```

>[!info] Permission Set Object
- **Description**: Defines permissions on objects.
- **Assignable**: Determines if the permission set can be assigned to users.
- **Non-Assignable**: Used as building blocks for functional assignable permission sets.

>[!example] Example: Permission Set
```al
permissionset 50134 "Sales Person"
{
    Assignable = true;
    Caption = 'Sales Person';
    Permissions = 
        tabledata Customer = RIMD,
        tabledata "Payment Terms" = RMD,
        tabledata Currency = RM,
        tabledata "Sales Header" = RIM,
        tabledata "Sales Line" = RIMD;
}
```
```al
permissionset 50130 MyPermissionSet 
{ 
    Assignable = true;
    Caption = 'My PermissionSet';
    IncludedPermissionSets = "Sales Person"; 
    Permissions = 
        codeunit SomeCode = x, 
        tabledata Vendor = RIM,
        codeunit AccSchedManagement = X; 
}
```

>[!info] Permission Set Extension Object
- **Description**: Adds permissions to an existing permission set.
- **Limitation**: Cannot remove permissions, only add.

>[!example] Example: Permission Set Extension
```al
permissionsetextension 50140 "Extended Sales Doc" extends "Sales Person"
{
    Assignable = true;
    Caption = 'Extended Sales Doc';
    Permissions =
        tabledata Currency = ID;
}
```

>[!tip] Generating/Updating Permission Sets
- **Command**: `al.generatePermissionSetForExtensionObjects`
- **Functionality**: Generates or updates permission sets as AL objects.
- **Alternative**: `al.generatePermissionSetForExtensionObjectsAsXml` for XML files.

### Tags
#entitlements #permissions #AL #Dynamics365 #BusinessCentral