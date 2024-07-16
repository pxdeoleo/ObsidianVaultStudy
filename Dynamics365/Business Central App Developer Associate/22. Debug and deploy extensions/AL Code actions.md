> [!summary]
> The [[AL Language Extension for VSCode|AL Language extension]] in [[Visual Studio Code for Business Central|Visual Studio Code]] provides code actions to help users correct issues in their AL code. These actions can be applied to single instances or broader scopes, enhancing efficiency in code refactoring.

#### Definitions
- **Code Actions**: Corrective measures provided next to an error or warning, represented by a light bulb icon.

> [!info] Available Code Actions
- Convert multiple IF statements to CASE.
- Spell check.
- Interface implementer.
- Make method local.
- Use parenthesis for method calls (instance, document, project, workspace).
- Fix explicit and implicit with statements.
- Update old report layout to rendering layout section.
- Fix for AW0013.
- Convert pages or page extensions to actionRef syntax for promoted actions (instance, document, project, workspace).

> [!info] Enabling AL Code Actions
1. **Via settings.json**:
    - Open Command Palette (Ctrl+Shift+P), search for and open settings.json.
    - Add `"al.enableCodeActions": true`.
    - Save the settings file.
2. **Via Settings Page**:
    - Open Settings (Ctrl+,).
    - Choose User Settings or Workspace Settings.
    - Navigate to Extensions > AL Language extension configuration.
    - Check the Enable Code Actions checkbox.

> [!tip] Larger Context Code Actions
- Some code actions can be applied to broader scopes, such as the entire document, project, or workspace, for more efficient refactoring.

> [!info] Code Actions Supporting Larger Scopes (2022 Release Wave 2)
- Convert promoted actions.
- AA0008 - Add parenthesis.
- AA0241 - To lowercase.
#### Tags
#ALLanguage #codeactions #VisualStudioCode #development #troubleshooting