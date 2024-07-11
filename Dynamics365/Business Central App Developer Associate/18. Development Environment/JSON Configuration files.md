> [!summary]
> JSON (JavaScript Object Notation) is a lightweight data interchange format. An AL extension for Dynamics 365 [[Business Central]] includes two JSON files: app.json and launch.json, used for configuration and deployment.

#### JSON Files in [[AL Language Extension for VSCode|AL Extension]]
- **launch.json**: Configures server information for testing and debugging.
- **app.json**: Contains extension metadata such as publisher, name, and supported versions.

> [!info] launch.json
- Specifies the object to start when the extension runs.
- Example: Page 22 (Customer List) as startupObjectId.
- Important properties include startupObjectId and startupObjectType.
- Reference for settings: [launch.json settings](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-launch-json-file).

> [!info] app.json
- Known as the manifest.
- Contains metadata like publisher, name, version, and dependencies.
- App identity includes app ID, which is auto-generated.
- Change ID if copying app or manifest from another app before publishing.
- Reference for settings: [app.json settings](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-app-json-file).

> [!info] App Identity and Management
- **ID**: Unique identifier; auto-generated or can be changed for new apps.
- **Name and Publisher**: Can be changed in Business Central 2021 release wave 2 or later, version must be incremented.
- **Version**: Incremented with each new app version uploaded to [[AppSource]] or as a per-tenant extension.
- **Dependencies**: Update in app.json if name or publisher changes in workspace projects.

>[!tip] Best Practices
- Use unique app IDs for sandbox and [[AppSource Publication for Business Central Apps|AppSource publishing]].
- Increment version on name or publisher change for 2021 release wave 2 or later.
- For versions prior to 2021 release wave 2, name and publisher cannot be changed after publishing.

#### Tags
#BusinessCentral #Extensions #ALCode #JSON #Development #MicrosoftDynamics #AppSource