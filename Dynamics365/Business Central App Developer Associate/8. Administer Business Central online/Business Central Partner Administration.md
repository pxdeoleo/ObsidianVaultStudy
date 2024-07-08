> [!summary] 
> As a Business Central partner, you can administer customer tenants through the Partner Center. You need to enroll in the Cloud Solution Provider program to manage administrative functions, including Windows upgrades.

#### Enrollment and Customer Management

- **Cloud Solution Provider Program**:
    - **Requirements**: MPN ID, business address, bank information, admin email.
    - **Instructions**: Follow detailed steps to complete enrollment.
- **Adding Customers**:
    - **Steps**:
        1. Navigate to "Customers" in Partner Center.
        2. Enter customer details and verify Microsoft Cloud Agreement.
        3. Select subscriptions and review entries.
    - **Free Trial**:
        - Customers can start with an evaluation version and extend trials up to 60 days.
        - Partners can extend trials beyond 60 days if necessary.

#### Administration Center

- **Access**:
    - **Roles**: Global Administrator, Dynamics 365 Administrator, Helpdesk Administrator.
    - **Partner Access**: Admin agent and helpdesk agent roles can access Business Central tenant as delegated administrators.
- **Functions**:
    - View and manage production/sandbox environments.
    - Set up upgrade notifications and view telemetry.
- **Direct URL Access**:
    - Format: `https://businesscentral.dynamics.com/[TENANT_ID]/admin`

#### Granular Delegated Admin Privileges (GDAP)

- **Security Feature**:
    - Provides least-privileged, time-bound access.
    - Customers no longer need to grant Global Admin privileges.
- **Roles**:
    - Dynamics 365 Administrator, Service Support Administrator, Helpdesk Administrator.
- **Management**:
    - Track user names and IDs in customer tenants.
    - Delegated admins are shown as unique IDs without personal information.
- **Restrictions**:
    - Delegated admins cannot run job queue entries or invite external accountants without customer approval.

#### Managing Delegated Permissions

- **Visibility**:
    - Delegated admins are not visible in the customer's Entra ID user list.
    - Actions performed are logged and associated with User ID in Business Central.
- **Revoke Access**:
    - Remove individual user access or revoke all partner rights from Microsoft 365 admin center.

#### Conditional Access and Security

- **Best Practices**:
    - Set up conditional access policies and require multifactor authentication for admins.
- **Restricting Access**:
    - Disable specific users within Business Central or revoke rights from all partner users without breaking the reseller relationship.