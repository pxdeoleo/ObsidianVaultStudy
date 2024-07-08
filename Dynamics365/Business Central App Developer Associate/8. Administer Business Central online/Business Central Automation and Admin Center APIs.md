> [!summary] 
> Business Central exposes several APIs for automating tasks and administration, enabling efficient company setup and tenant management.

> [!info] Automation APIs

- **Purpose**: Automate company setup and tenant hydration.
    
- **Common Tasks**:
    
    - Create new companies
    - Run RapidStart packages
    - Install extensions
    - Add users to user groups
    - Assign permission sets to users
- **Authentication**:
    
    - Delegated admin credentials
    - Dynamics 365 Business Central users with appropriate permissions
- **Namespace**: `microsoft/automation API`
    

> [!example] API List

- **Automation company**
- **Company**
- **Configuration package**
- **Extension**
- **Extension deployment status**
- **Extension upload**
- **Permission set**
- **Profile**
- **Scheduled job**
- **User**
- **User group**
- **User group member**
- **User group permission**
- **User permission**

> [!info] Business Central Admin Center API

- **Purpose**: Enable administrators to programmatically perform administrative tasks for a Business Central tenant.
- **Common Tasks**:
    - Query and manage production and sandbox environments
    - Set up administrative notifications
    - View telemetry for tenant events

> [!example] Authentication Methods

- **Service-to-Service Microsoft Entra apps**: Client Credentials Flow
- **Microsoft Entra ID based authentication**: Authorization Code Flow

> [!info] Error Handling

- **Error Object**: Standard structure, varies by endpoint and error.
- **Common Issues**:
    - Request sending failures
    - Authentication problems
    - API not receiving the request