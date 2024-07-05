> [!summary] 
> Business Central environments consist of Microsoft and third-party apps working together to meet various business needs. Regular updates add new features and fix issues. The Manage Apps page in the administration center helps manage these updates without the need for uninstallation and reinstallation.
#### Definitions

- **Business Central Environment**: A collection of Microsoft and third-party apps.
- **Manage Apps Page**: An admin center feature for managing app updates.

> [!info] Updates and Management

- Regular updates add new features and fix issues.
- Updates can be managed by partners (delegated administrators) or local customer administrators.

> [!bug] Avoid Uninstallation

- Moving to the new FAME service means no need for uninstallation and reinstallation to update apps.
- Cleaner way to manage app updates.

> [!info] Availability of Update Feature

- Gradual rollout of the update feature in the administration center.
- Check the timeline for full availability.

> [!example] Check for Updates

1. Open Manage Apps from the environment details page.
2. Select Environments > select the environment > Manage Apps.
3. The Manage Apps page lists installed apps and checks for updates upon opening.

> [!info] Indications of Available Updates

- **Latest Available Version**: Shows the new version number.
- **Available Update Action**: Displays actions such as "Action required" or "Install update".

> [!tip] Install Updates on Sandbox First

- Test updates on a Sandbox environment to avoid disruptions.
- Create a Sandbox if you don't have one.

> [!example] Install an App Update

1. Open Sandbox environment and select Manage Apps.
2. Resolve any "Action required" links.
3. Select "Install update" to install the new version.
4. Confirm the installation and refresh to check status.
5. Test the new version in Sandbox before updating production.

> [!info] Resolving Update Requirements

- **Update Requirements**: Lists existing apps that need updates.
- **Install Requirements**: Lists new dependency apps that need installation.

> [!info] Update Installation Process

- The new version installs immediately after confirmation.
- Minimal user interruption, recommended to install outside working hours.

> [!info] Handling Update Failures

- **Update failed** action appears if installation fails.
- Retry the update or contact ISV/Microsoft support with the Operation ID.