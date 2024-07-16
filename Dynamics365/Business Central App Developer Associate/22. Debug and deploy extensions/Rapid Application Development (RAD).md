>[!summary]
Rapid Application Development (RAD) in [[Visual Studio Code for Business Central|Visual Studio Code]] facilitates faster development on large Business Central projects by compiling and publishing only changed application objects. RAD is an interim state that does not replace a full publish.

#### Definitions
- **RAD**: A method to accelerate development by only compiling and publishing changes made during a development session.

>[!info] RAD File
- Contains changes made by the developer in a `.rad` file located in the `.vscode` folder.
- Includes application objects, page customization objects, and profile objects.
- Excludes translation files, permission files, custom word and report RDL layout files, table data, and web service definitions.

>[!tip] RAD Publishing Shortcuts
- **Ctrl+Alt+F5**: Start RAD publishing without debugging.
- **Alt+F5**: Start RAD publishing with debugging.

>[!bug] RAD Changes Persistence
- RAD changes are only saved during build, publish, or debug actions.
- Closing Visual Studio Code without saving, building, publishing, or debugging will result in loss of RAD changes.

>[!attention] Full Publishing
- Use **Ctrl+F5** for full publishing to regenerate all necessary files.
- A RAD file is deleted after successful publishing to ensure the package is complete.

#### Best Practices
- Regularly perform a full publish to ensure all components are included.
- Check the `.rad` file to review which application objects are changed before publishing.

#### Tags
#RAD #VisualStudioCode #BusinessCentral #Development #Publishing