### 1. Structural Hierarchy:

- **Elements:** Fundamental components, such as metadata and source files (e.g., base enumerations, tables). Available out-of-the-box or can be created in [[Application Explorer]] (AOT).
- **Models:** Collections of elements (e.g., warehouse management model). Organized within projects.
- **Packages:** Aggregations of models, used to create deployable packages.
### 2. Diagram & Visuals:

- Technical architecture of elements.
- [[Application Explorer]] interface in Visual Studio.

### 3. Development Process:

#### Creating Models:
- Navigate: Dynamics 365 menu > Model Management > Create model.
- Input: Model name, publisher, layer, description, display name.
- Steps: Select options for new package, reference models, and confirm details.
#### Building Models:
- Navigate: Dynamics 365 menu > Build models.
- Selection: Choose packages and associated models, opt for building referenced packages.
- Options: Choose build processes like pre-compiled forms, reports, best practice checks, database synchronization.

#### 4. Deployable Packages:

- Creation and deployment through [[Lifecycle Services]].
- Contains multiple packages for runtime environments.
- Represents UI modules (e.g., Accounts Payable) including all fields, menus, and pages.

#### 5. Source Control:

- Required for managing elements and development, typically using Azure DevOps.

### Key Actions:

#### To Create a New Model:

1. Open the Create model wizard from the Dynamics 365 menu.
2. Enter relevant model details and select package creation options.
3. Choose referenced models and finalize settings.
4. Optional: Create a new project and set as default for new projects.
5. Finish setup.

#### To Build Models:

1. Initiate build from the Dynamics 365 menu.
2. Select packages to build and set options for build processes.
3. Review build details in the Details tab.