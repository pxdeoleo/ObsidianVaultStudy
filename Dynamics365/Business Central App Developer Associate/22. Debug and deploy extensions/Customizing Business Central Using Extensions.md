>[!summary]
You can customize [[Business Central]] by installing apps that add functionality, change behavior, or provide access to new services.

#### Definitions
- **Extensions**: Apps that modify or enhance Business Central functionality.

>[!info] Permissions
- To install/uninstall apps, you need to be in the D365 Extension MGT user group or have the EXTEND. MGT. - ADMIN permission set.
- Administrators can assign these permissions to other users.

>[!info] Using Extensions
- Assign the permission sets that come with the extension to use its functionalities (pages, reports, actions, etc.).

#### Installation Process

>[!example] Install an Extension
1. Go to the Extension Management page from Home or use the Search for Page or Report icon.
2. Access new apps from AppSource.microsoft.com, using the same email as for Business Central.
3. From Business Central, access the Extension Marketplace via the Extension Management page.
4. Select and get an app, agreeing to its terms of use.
5. Complete installation in Business Central if initiated from AppSource website.

>[!tip] Setting Up Apps
- After installation, some apps require setup (e.g., providing information like PayPal account details).
- Business Central may prompt for setup immediately after installation or allow setup later from the Installed Extensions page.

>[!info] AppSource Marketplace
- AppSource provides apps for Business Central and other Microsoft products. It can be accessed directly or via Business Central.

#### Managing Apps

>[!example] Upload a Per-Tenant Extension (PTE)
1. On the Extension Management page, go to Manage > Upload Extension.
2. Specify the .app file and choose Accept, then Deploy.
3. If needed, use Schema Sync Mode's Force option for breaking schema changes.

>[!example] Uninstall an App
1. On the Extension Management page, select the app and choose Uninstall.
2. To keep data: data isn't deleted by default; it remains if the app is reinstalled.
3. To delete data: toggle on Delete Extension Data before confirming uninstallation.
4. Note dependent apps: must uninstall dependents first.
5. Required apps: some cannot be deleted via the Extension Management page.

>[!attention] Important Considerations
- Deleting data: irreversible once the Delete Extension Data toggle is on.
- Dependent apps: must be uninstalled if the main app is removed.
- Required apps: some cannot be uninstalled.

#### Microsoft Provided Apps
- Examples: AMC Banking 365, Ceridian Payroll, PayPal Payments Standard, QuickBooks Data Migration, Sales and Inventory Forecast, etc.

#### Tags
#BusinessCentral #Extensions #AppSource #Customization #Permissions