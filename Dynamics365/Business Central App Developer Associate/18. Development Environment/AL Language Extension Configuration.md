> [!summary]
> The [[AL Language Extension for VSCode|AL Language extension for Visual Studio Code]] includes settings for both user and workspace configurations. Key features include code analysis, AL Home, and AL Explorer, which aid in developing, navigating, and understanding AL code for Dynamics 365 [[Business Central]].

#### Configuring AL Language Extension
- **Access Settings**: 
  - **Workspace Settings**: Ctrl+Shift+P, Preferences: Open Settings (UI)
  - **User Settings**: Ctrl+Shift+P, Preferences: Open User Settings
- **Enable Code Analysis**: 
  - Default: false
  - Set to true to enable code analysis with specified code analyzers.

> [!info] AL Home
- Displays news, best practices, events, urgent info, and learning content.
- Default setting shows AL Home when updated.
- Change default:
  - Workspace Settings: Ctrl+Shift+P, Preferences: Open Settings (UI)
  - User Settings: Ctrl+Shift+P, Preferences: Open User Settings
  - Modify "Show Home at startup" value.

> [!info] AL Explorer
- Provides an overview of objects, dependencies, and extension points.
- Four tabs: OBJECTS, EVENTS, APIS, EXTENSIBLE ENUMS.
- Features:
  - Filter, bookmark, and run objects.
  - View high-level structures and perform light troubleshooting.
  - Source button for code access and breakpoints.
  - Subscribe button in EVENTS for code snippets.
  - Access control may restrict full source code visibility.
#### AL Explorer Tabs
1. **OBJECTS**: Filter, bookmark, and run tables, pages, reports.
2. **EVENTS**: Overview of events and extension points.
3. **APIS**: Overview of APIs.
4. **EXTENSIBLE ENUMS**: Overview of extensible enums.
#### Usage Tips
- Use bookmarks for frequently used objects.
- Use filtering for focused navigation.
- Source button helps with code development and troubleshooting.
#### Tags
#BusinessCentral #ALExtension #ALHome #ALExplorer #VisualStudioCode #Settings #CodeAnalysis #Development #MicrosoftDynamics