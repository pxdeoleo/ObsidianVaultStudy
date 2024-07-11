>[!summary]
>For tenant-specific customizations or per-tenant extensions in Microsoft Dynamics 365 [[Business Central]], developers must proactively manage the lifecycle and compatibility of their extensions with ongoing Business Central updates to ensure uninterrupted service.

#### Definitions
- **Tenant-Specific Customization**: Modifications or extensions tailored to a single Business Central tenant.
- **Per-Tenant Extension**: An extension developed specifically for one tenant's Business Central environment.

>[!info] Lifecycle of Per-Tenant Extensions
- Developers are responsible for updating extensions and ensuring compatibility with new versions of the Business Central base application.

>[!bug] Challenges with Extension Updates
- Ensuring that extensions do not break with new updates can be challenging, requiring diligent management and timely updates.

>[!info] Automated Extension Validation Process
- Before a scheduled update, an automated service validates each tenant customization to check compatibility with the new version of Business Central.

>[!tip] Handling Update Notifications
- Configure notification recipients in the Business Central administration center to receive crucial updates and compatibility alerts.

>[!attention] Impact of Incompatible Extensions
- Updates to Business Central environments may be blocked if extensions are found incompatible, necessitating immediate developer intervention.

>[!example] Steps to Manage Extension Compatibility
1. **Monitor Compatibility**: Regularly check your extension against upcoming Business Central updates.
2. **Respond to Notifications**: Act swiftly on notifications regarding incompatibilities.
3. **Update Extensions**: Provide necessary updates to maintain compatibility with the base application.

>[!info] Notification and Failure Handling
- If an extension fails compatibility checks, detailed notifications guide developers on required updates. If updates are not made, the extension may be automatically removed to allow Business Central updates.

>[!info] Preventing Automatic Extension Removal
- Ensure your extension remains compatible within 90 days from the first notification to avoid automatic removal and disruption of the tenant's operations.