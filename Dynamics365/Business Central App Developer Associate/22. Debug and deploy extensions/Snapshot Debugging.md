>[!summary]
Snapshot debugging is a method in [[Visual Studio Code for Business Central|Visual Studio Code]] for troubleshooting [[Business Central]] cloud production environments, enabling consultants to investigate code execution issues directly in the production tenant.

#### Definitions
- **Snapshot debugging**: Debugging method that records AL code execution on a server for later offline inspection in Visual Studio Code.

>[!info] Snapshot Debugging Features

- **Snappoints**: Breakpoints that do not stop code execution but log state for offline inspection.
- **Snapshot Attach Configuration**: Defines how the snapshot attaches to the environment (web client, API, background session).
- **Session Types**:
  - **WebClient**
  - **Web API**
  - **Background session**

>[!example] Snapshot Debugging Workflow

1. **Set Snappoints**: Place snappoints in the code.
2. **Create Configuration**: Define user ID, session ID, and snapshot verbosity in the configuration file.
3. **Attach Environment**: Attach to the environment in snapshot mode.
4. **Perform Actions**: Execute the steps to trigger snappoints.
5. **Download Snapshot**: Retrieve the snapshot file after reproduction.
6. **Inspect Snapshot**: Analyze the stack trace and variables in Visual Studio Code.

>[!info] Session States

- **Initialized**: Server waiting for a session to debug.
- **Started**: Attached to an end-user session.
- **Finished**: Debugging session completed.
- **Downloaded**: Snapshot file downloaded for inspection.

>[!tip] Permissions

- **Delegated Admin**: Must be part of the D365 Snapshot Debug permission group.
- **Symbols Matching**: Ensure symbols on the server match local symbols for accurate debugging.

#### Practical Tips

- **Snapshot Configuration**:
  - `"userId"`: User GUID.
  - `"sessionId"`: Session ID.
  - `"snapshotVerbosity"`: Level of execution context recorded.
- **Initializing Snapshot**: Use `Ctrl+Shift+P` and select `AL: Initialize Snapshot Debugging`.

>[!info] AL Profiler

- **Profile File Generation**: Analyze performance using top-down or bottom-up call stack views.
- **Execution Context**:
  - **Debug**: No profiling.
  - **Profile**: Profiling only.
  - **DebugAndProfile**: Both profiling and debugging.

>[!tip] Visual Cues

- **Code Lines Executed**: Vertical lines in the left gutter of Visual Studio Code during snapshot playback.
- **Customization**: Control gutter bar color using `al.snapshotDebuggerLinesHitDecoration`.

#### Tags
#snapshotdebugging #businesscentral #troubleshooting #visualstudiocode