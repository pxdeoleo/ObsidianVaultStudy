> [!summary]
> [[Visual Studio Code for Business Central|Visual Studio Code]]'s multi-root workspace feature supports working with multiple AL projects simultaneously, allowing project grouping and shared configurations.

#### Definitions
- **Multi-root workspace**: A feature in Visual Studio Code that allows grouping multiple project folders into a single workspace.
- **AL Language extension**: Supports multi-root functionality, enabling work with multiple AL project folders in one workspace.

> [!info] Workspace Setup
1. **Add Folder to Workspace**: On the File tab, choose "Add Folder to Workspace...".
2. **Save Workspace File**: Save the code-workspace file to reopen it easily. It contains an array of folders with absolute or relative paths. Use relative paths for sharing.
3. **Modify Settings**: Change user settings, global workspace settings, or individual folder settings in the Settings editor.

> [!tip] Mixed Project Types
- It's not mandatory to use only AL-based roots. Different types of projects can be included, and each AL project will have its own configuration settings:
  - **al.packageCachePath**: Specifies the cache path for symbol files.
  - **al.enableCodeAnalysis**: Enables code analyzers for the project.

> [!info] Project References
- Defined as dependencies in the app.json file with full id, name, publisher, and version.
- No special visual representation for project references.
- Changes to project name or publisher require updates in the app.json file.

> [!example] Dependency Definition
- Example: Leaf project depends on Middle and Root projects within the workspace. No need to download symbols for project references; they resolve automatically.

> [!info] Building Projects
- **Build Process (Ctrl+Shift+B)**:
  1. .app file is copied to the .alpackages folder of dependent projects.
  2. All "dirty" project references are built.
- **Reference Resolution Issues**: Rebuild project reference and reload workspace to resolve.

> [!info] Project Loading
- Projects load their references transitively.
- Features like IntelliSense are unavailable during loading.
- Notifications indicate loading status and can be closed without stopping the process.
- Switching projects cancels the current loading and starts the new one.

> [!tip] Publishing Logic
- **Set Publishing**:
  - Performed for all changed projects with a defined startup project.
  - Dependencies are included based on changes in application objects.
- **Dependency Publishing Options (launch.json)**:
  - **Default**: Set dependency publishing.
  - **Ignore**: Skips dependency publishing (use with caution).
  - **Strict**: Fails if any installed apps depend on the startup project.
- Use **AL: Publish full dependency tree for active project** to traverse and install required dependencies.

> [!tip] Incremental Builds
- **al.incrementalBuild**: Set to true for faster build times by resolving from referenced projects instead of the \packagecache folder.

#### Tags
#vscode #multi-root #ALlanguage #projectmanagement #dependencies #publishing #settings