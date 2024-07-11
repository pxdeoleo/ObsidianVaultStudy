>[!summary] 
Updating your app for [[Business Central]] involves submitting the updated app file to Partner Center, undergoing validation, and ensuring version compatibility. Follow best practices to manage versioning, dependencies, and hotfixes.

#### Definitions
- **App Update**: The process of submitting a new version of your app to Business Central.
- **[[AppSource]]**: The marketplace where Business Central apps are published and updated.

>[!info] Update Process
- Submit the updated app file to Partner Center.
- Undergo a scaled-back validation process.
- Increase the version number in the app's json manifest files.
- Keep the app's App ID the same across versions.

>[!info] Availability and Compatibility
- Updated apps become active upon passing validation and being checked into the service.
- Tenants get the latest compatible version of the app for their Business Central version.
- Compatibility is ensured against the latest Business Central version at the time of submission.

>[!example] Versioning Example
- Submit app when Business Central is at version 16.1.
- App is compatible with version 16.1 and configured for future versions.
- Tenants on earlier versions get the compatible app version for their Business Central version.

>[!tip] Managing App Updates
- **Avoid Frequent Updates**: Bundle bug fixes and features to minimize update frequency. Aim for a minimum one-month update cadence.
- **Hotfixes**: Critical hotfixes are prioritized. Follow the hotfix process on AppSource.

>[!info] Auto-Updates
- **Minor Releases**: Apps are not auto-updated unless they would break in the release.
- **Major Releases**: All apps are auto-updated to the latest version.

>[!example] Updating Installed Apps
- Tenants uninstall and reinstall the app to get the latest version.
- Future updates may be managed via the new Manage Apps page in the Business Central administration center.

>[!info] Library App Changes
- Submit the updated library app to Partner Center.
- Main app remains unchanged if dependencies meet the minimum version requirement.

>[!example] Dependency Versioning
- Main app specifies "version 1.0.0.1 or greater" for the library app.
- Updated library app versions (e.g., 1.0.0.2) are compatible without changing the main app's json file.