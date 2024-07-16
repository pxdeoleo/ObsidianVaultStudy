>[!summary]
>**Attaching the AL Debugger** enables debugging of AL code in Business Central by connecting to existing or new sessions. This requires configuration in `launch.json` and proper permissions.

#### Definitions
- **AL Debugger**: A tool in [[Visual Studio Code for Business Central|Visual Studio Code]] for debugging AL language code in Business Central.
- **Attach Debugging PermissionSet**: A permission set that allows debugging on behalf of another user.

>[!info] Session Attachment
- You can attach the debugger to:
  - An existing running session.
  - The next session for a specific user.

- Requires configuration in `launch.json` using session ID or user ID.

>[!info] Permissions
- New **Attach Debugging PermissionSet** allows cross-user debugging.
- The user starting the Visual Studio Code attach session must issue the Web request on the server.

>[!tip] Publishing App
- Ensure the app is published with `Ctrl+F5` or `Alt+Ctrl+F5` for RAD publishing before starting the debugging session.

>[!example] Example Configuration for Local Server
```json
{
    "name": "My attach to local server",
    "type": "al",
    "request": "attach",
    "server": "https://localhost",
    "serverInstance": "BC200",
    "authentication": "Windows",
    "breakOnError": true,
    "breakOnRecordWrite": false,
    "enableSqlInformationDebugger": true,
    "enableLongRunningSqlStatements": true,
    "longRunningSqlStatementsThreshold": 500,
    "numberOfSqlStatements": 10,
    "breakOnNext": "WebClient"
}
```

#### Configuration Steps
1. **Add Configuration**: In Visual Studio Code, navigate to `Run > Add configuration`.
2. **Select Session Type**: Choose to attach to a cloud or local session. Adjust the `server` and `serverInstance` settings for local sessions.
3. **Set Breakpoint**: Define the `breakOnNext` property for the client type to break on.
4. **Add Breakpoints**: In your code, set at least one breakpoint using the `Run` toolbar.
5. **Publish App**: Ensure the app is published using `Ctrl+F5` or `Alt+Ctrl+F5` for RAD publishing before starting the session.
6. **Start Session**: Press `F5` to start the debugging session.
7. **Debug**: Inspect the code and add more breakpoints as needed.
8. **Stop Session**: Select `Detach` in the Visual Studio Code toolbar to stop debugging.

#### Tags
#aldebugger #businesscentral #debugging #launchjson #crossuserdebugging