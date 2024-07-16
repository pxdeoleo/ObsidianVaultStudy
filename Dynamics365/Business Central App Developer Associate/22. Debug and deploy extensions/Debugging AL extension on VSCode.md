> [!summary]
> Debugging is the process of finding and correcting errors in code. [[Visual Studio Code for Business Central|Visual Studio Code]] with the [[AL Language Extension for VSCode|AL Language extension]] provides an integrated debugger to inspect code and ensure applications run as expected.

#### Definitions
- **Debugger:** Tool to inspect and correct code.
- **Breakpoint:** A marker to pause execution at a specific code line.

> [!info] Debugging Session
- Start with F5 key.
- External code can only be debugged if `showMyCode` flag is set in `app.json`.
- Each F5 press launches a new client instance.
- Closing the session requires closing web client instances.
- Pausing the session isn't supported.

> [!info] Breakpoints
- Basic concept: set on a statement to pause execution.
- Set via Debug menu or F9 key.
- Step into base application code using Go to Definition (F12) and set breakpoints in the referenced code (.dal files).

#### Breakpoints on External Code
1. Create a variable of a base object or select the SourceTable.
2. Right-click the variable and select Go to Definition, or press F12.
3. In the .dal file, select a line and press F9.

> [!tip] Debugging Shortcuts
- F5: Start debugging
- Ctrl+F5: Start without debugging
- Shift+F5: Stop debugging
- Ctrl+Shift+F5: Start debugging without publishing
- Alt+F5: Start Rapid Application Development with debugging
- F10: Step over
- F11: Step into
- Shift+F11: Step out
- F12: Go to Definition

> [!info] Break on Errors
- Set in `launch.json` with `breakOnError` property.
- Values: `true` (All), `false` (None), `None`, `All`, `ExcludeTry`.
- `true` and `false` retained for backward compatibility; use `All` and `None` instead.

> [!info] Break on Record Changes
- Set in `launch.json` with `breakOnRecordWrite` property.
- Values: `true` (All), `false` (None), `None`, `All`, `ExcludeTemporary`.
- `true` and `false` retained for backward compatibility; use `All` and `None` instead.

> [!info] Resource Exposure Policy Settings
- Default protection against downloading/debugging in `app.json`.
- `resourceExposurePolicy` options: `allowDebugging`, `allowDownloadingSource`, `includeSourceInSymbolFile`.
- Example default setting: 
  ```json
  "resourceExposurePolicy": { 
    "allowDebugging": true, 
    "allowDownloadingSource": false, 
    "includeSourceInSymbolFile": false 
  }
  ```

> [!info] allowDebugging
- Set `allowDebugging` to `true` to enable debugging.
- Default is `false`.
- Overrides allowed by setting resource policy.

> [!info] allowDownloadingSource
- Set `allowDownloadingSource` to `true` to allow downloading source code.
- Default is `false`.

> [!info] includeSourceInSymbolFile
- Set `includeSourceInSymbolFile` to `true` to include source in symbol files.
- Default is `false`.

> [!info] AL Compiler Diagnostic Messages
- Diagnostic messages include URLs for documentation.
- Feedback needed to improve documentation.

> [!example] Launch in a Specific Company
- Use `startupCompany` parameter in `launch.json` to specify the company for debugging.

> [!info] View SQL Server Information
- Database Statistics in Variables window shows SQL locks during AL debugging.
- Helps understand database locks and last executed SQL statements.

> [!info] Debug the System Application
- Debugging of the System application enabled, except for SecureText type protected variables.
- Useful for development, troubleshooting, and Open Source contributions.

#### Tags
#debugging #visualstudiocode #allanguage #breakpoints #resourceexposure #sqlserver #systemapplication