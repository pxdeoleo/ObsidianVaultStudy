> [!summary]
> Dynamics 365 [[Business Central]] functionality is coded in objects using Application Language (AL) code, stored in .al files. Developers create extensions to modify or add new functionality. Extensions are compiled into .app packages for deployment. The AL Language extension in Visual Studio Code facilitates extension development with modern development environment features.

#### Creating Extensions
1. **[[AL Language Extension for VSCode|Install AL Language Extension]]**: Use Visual Studio Code Marketplace.
2. **Start a New Extension**: 
    - Open Visual Studio Code.
    - Use Command Palette (Ctrl+Shift+P) and enter AL: Go.
    - Choose a storage path and target Business Central version.
    - Select the server instance (cloud sandbox or local server).
    - Provide user credentials to download reference symbols.

> [!info] Downloading Symbols
- Symbols are .app files downloaded to .alpackages folder.
- Contains references for objects (e.g., fields in tables, page layouts).
- Use AL: Download Symbols command if not downloaded automatically.

> [!info] Deployment
- Press F5 to deploy and launch Business Central in a web browser.
- Debugging session starts; stop debugging with the red Stop icon in Visual Studio Code.

> [!info] File Management
- **HelloWorld.al**: Default file created with new extension; recommended to delete it.
- **Microsoft_Application.app**: Encapsulates all extensions; referenced in app.json using Application version property.
- **NoImplicitWith**: Default in new projects to encourage explicit WITH statements.
- **OutFolder Property**: Specifies output folder for generated app files; useful for managing multiple apps.

>[!Managing Extensions]
- **Prefix/Suffix**: Ensure unique object names; use AppSourceCop tool for detection.
- **Object Numbering Conventions**: Follow guidelines for object ranges (e.g., 50,000-99,999 for tenant customizations).

>[!Customization and Contributions]
- Developers can extend tables, pages, reports, code flows, and security model.
- Contribute to open-source projects for system application modules.
- Follow module architecture guidelines for consistency and reliability.

#### Documentation
- [Get started with modules in the System Application](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-get-started-system-application)
- [Set Up an Environment for Developing a Module](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-develop-environment)
- [Create a new module in the System Application](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-create-system-application-module)
- [Create a .NET Wrapper Module](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-create-dotnet-wrapper)
- [Change a module in the System Application](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-change-system-application-module)

#### Tags
#BusinessCentral #Extensions #ALCode #Development #MicrosoftDynamics #VisualStudioCode #Symbols #Deployment #Customization #ModuleArchitecture #[[AppSource]]