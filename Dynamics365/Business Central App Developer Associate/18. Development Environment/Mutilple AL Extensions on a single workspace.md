> [!summary]
> [[Visual Studio Code for Business Central|Visual Studio Code]] supports multi-root workspaces, allowing you to group and manage multiple project folders within one workspace. The AL Language extension is compatible with this feature, facilitating simultaneous work on several related AL projects.
#### Setting Up Multi-Root Workspace
1. **Add Folders to Workspace**:
   - Go to File tab in Visual Studio Code.
   - Select "Add Folder to Workspace..." to include other AL project folders.
2. **Save Workspace**:
   - Save the workspace file for future use.
   - Creates a .code-workspace file with folder paths (absolute or relative).
   - Use relative paths for sharing workspace files.

> [!info] Settings Configuration
- Modify settings via the Settings editor.
  - User settings
  - Global workspace settings
  - Individual folder settings
#### Benefits of Multi-Root Workspaces
- Group related AL projects in a single workspace.
- Streamline development workflow by switching between projects easily.
- Centralize settings management for multiple projects.
#### Example Steps
1. **Adding a Folder**:
   - Navigate to File > Add Folder to Workspace...
   - Select the desired AL project folder.
   - Repeat for additional folders.
2. **Saving the Workspace**:
   - Save the workspace configuration.
   - Ensure the .code-workspace file is created with the desired paths.

> [!tip] Sharing Workspace
- Use relative paths in the .code-workspace file for easy sharing.
#### Tags
#VSCode #ALCode #MultiRootWorkspace #Development #BusinessCentral