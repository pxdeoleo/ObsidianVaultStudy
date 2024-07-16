>[!summary]
The `resourceExposurePolicy` in the `app.json` file defines the accessibility of resources and source code during various operations for an extension project.

#### Definitions
- **resourceExposurePolicy**: Specifies the areas where the source code of an extension can be accessed. Options include:
  - `applyToDevExtension`
  - `allowDebugging`
  - `allowDownloadingSource`
  - `includeSourceInSymbolFile`

>[!info] Default Settings
- All options are set to `false` by default, preventing dependent extensions from debugging or downloading the source code.

>[!code] Syntax
```json
"resourceExposurePolicy": {
  "applyToDevExtension": <boolean>,
  "allowDebugging": <boolean>,
  "allowDownloadingSource": <boolean>,
  "includeSourceInSymbolFile": <boolean>
}
```

>[!example] AL:Go! Project Template
- The template sets `allowDebugging`, `allowDownloadingSource`, and `includeSourceInSymbolFile` to `true` by default.

#### Options Explained

>[!info] applyToDevExtension
- Applies resource exposure policies to developer extensions if set to `true`.

>[!info] allowDebugging
- Enables debugging into the extension when set to `true`.
- Requires the `allowDebugging` flag to be set in the dependency extension's `app.json`.
- **Note**: Profiles, Page Customizations, and Views are excluded from this setting.

>[!bug] [NonDebuggable] Attribute
- Prevents debugging of methods and variables marked with this attribute, even if `allowDebugging` is `true`.

>[!info] allowDownloadingSource
- Allows the source code and media files to be downloaded when set to `true`.

>[!info] includeSourceInSymbolFile
- Includes source code in the downloaded symbol file when set to `true`.

#### Override the Resource Policy

>[!example] Dynamic Overrides
- Use the `BC-ResourceExposurePolicy-Overrides` secret in a key vault to dynamically grant access to users.
- Example of JSON structure for the secret:
  ```json
  {
    "allowDebugging": [ "tenantID" ],
    "allowDownloadingSource": [ "tenantID" ],
    "includeSourceInSymbolFile": [ "tenantID" ]
  }
  ```
- Define the secret using Azure PowerShell to handle multi-line JSON.

#### Tags
#resourceExposurePolicy #appjson #development #troubleshooting