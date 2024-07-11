> [!summary]
> AL developers can extend [[Business Central]] by modifying tables, pages, reports, code flows, and the security model. Contributions can also be made to open-source projects for system application modules. Business Central's architecture includes the System Application and Base Application layers.

#### Layers of Business Central Application
- **System Application**: Open-source modules for building, maintaining, and upgrading apps.
- **Base Application**: Business logic for Business Central functionality.

> [!info] System Application
- Interacts with the Business Central platform.
- Supports business logic in the Base Application.
- Overview available: [System Application modules](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-system-application-overview).

> [!info] System and Base Application Reference
- Lists all objects in the system and base application layers.
- Includes obsoleted objects by type.
- Reference available: [System and Base Application Reference](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-system-application-reference).

> [!info] Module Architecture
- Independent projects with app.json files.
- Belong to specific packages or functional layers.
- Modules in higher layers can only depend on lower or same-layer modules.
- Facade codeunits, pages, and tables are publicly accessible; internal implementation details are not.

#### Facade Rules
1. Access must be Public.
2. Integration and business event publishers as internal functions.
3. Event publishers marked internal, exceptions documented.
4. External methods in the facade.
5. No logic or local functions in the facade.
6. Meaningful, short names for facades; internal codeunits can use "Impl" suffix.

#### Extensibility
- Extensibility thought into the internal implementation of modules.
- Extensibility property set to False to prevent extensions if not desired.

#### Documentation for Developing Modules
- **Get started with modules in the System Application**: [Link](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-get-started-system-application)
- **Set Up an Environment for Developing a Module**: [Link](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-develop-environment)
- **Create a new module in the System Application**: [Link](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-create-system-application-module)
- **Create a .NET Wrapper Module**: [Link](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-create-dotnet-wrapper)
- **Change a module in the System Application**: [Link](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-change-system-application-module)

#### Contributing to the System Application
- Determine the type of contribution:
  - Small bug fixes, product improvements, customer conveniences.
  - New capabilities or larger changes.
- Contribution information: [Contributing to Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-contribute-system-application).

#### Tags
#BusinessCentral #Development #SystemApplication #BaseApplication #Modules #Extensions #MicrosoftDynamics #Architecture #OpenSource #Contribution