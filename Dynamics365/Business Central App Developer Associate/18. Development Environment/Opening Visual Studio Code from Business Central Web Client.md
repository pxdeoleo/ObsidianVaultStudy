>[!summary]
With [[Business Central]] 2023 release wave 2, you can open a new Visual Studio Code session directly from the web client for troubleshooting, debugging, inspecting variables, setting breakpoints, and viewing source code.

#### Definitions
- **Business Central Web Client**: Interface used for accessing Business Central functionalities.
- **[[Visual Studio Code for Business Central|Visual Studio Code]]**: Source-code editor for debugging and editing code.
- **Resource Exposure Profile**: Settings that control access to source code for each extension.

>[!info] Methods to Open Visual Studio Code
- **From Page Inspector**: Open page code from the Page Inspection page.
- **From Help and Support**: Attach debugger to the current session via the Help and Support page.

>[!example] Open Page from Page Inspector

1. Locate the page to inspect in the Business Central web client.
2. Run Page Inspection with `Ctrl+Alt+F1`.
3. Select **Explore page in Visual Studio Code** link.
4. Choose **Open** in the **Allow an extension to open this URI?** dialog.
5. Decide to create a new project or use an existing one.
6. Choose to download symbols if needed.
7. Select the type of debugging session (snapshot or regular).
8. Set breakpoints and inspect the code in Visual Studio Code.

>[!example] Inspect a Specific Field

1. Locate the page with the desired field.
2. Run Page Inspection with `Ctrl+Alt+F1`.
3. Choose the field to inspect and select **Explore field in VS Code**.

>[!example] Troubleshoot from Help and Support

1. Navigate to the Help and Support page in the Business Central web client.
2. Choose **Attach debugger to this session** link under Troubleshooting.
3. Open Visual Studio Code via the **Allow an extension to open this URI?** dialog.
4. Decide to create a new project or use an existing one.
5. Set breakpoints and inspect the code in Visual Studio Code.

>[!attention] Debugging Restrictions

- Regular debugging is not supported for production environments.
- If the AL Language extension is not installed, the process ends.

>[!tip] Maintain Projects

- Regularly delete unused projects to avoid clutter.

>[!info] Visual Studio Code Sessions

- If already open, the last active session is used.
- Requires AL Language extension for functionality.
- Ensure source files are up to date for accurate debugging.

>[!tip] Administrator Mode

- Run Visual Studio Code as an administrator to handle updates and permissions issues.

#### Tags
#BusinessCentral #VisualStudioCode #Debugging #Troubleshooting