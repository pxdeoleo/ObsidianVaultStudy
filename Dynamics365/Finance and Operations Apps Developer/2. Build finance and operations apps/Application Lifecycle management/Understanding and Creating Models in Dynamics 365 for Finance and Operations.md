>[!summary]
>Models in Dynamics 365 for Finance and Operations are essential for managing customizations and ensuring seamless deployment of solutions. This note provides an overview of how to design, create, and manage models within the development environment.

#### Definitions
- **Model**: A collection of elements like metadata and source files that define a part of a solution in Dynamics 365.

>[!info] Importance of Models
- Models organize customizations and extensions.
- They are packaged into deployable packages for application across different environments.

>[!bug] Common Challenges with Models
- Managing dependencies between models can be complex.
- Overlays in models can complicate application updates and maintenance.

#### Creating Models in Visual Studio

>[!example] Steps to Create a Model
1. **Access the Create Model Wizard**:
   - Navigate to the Dynamics 365 menu in Visual Studio.
   - Choose 'Create model' under Model Management.
2. **Choose Model Type**:
   - **Own Package**: Ideal for new solutions needing separate deployment.
   - **Existing Package**: Adds to an existing package but may complicate updates due to overlays.
3. **Configure Model Parameters**:
   - Set model name, description, and dependencies.
   - If creating a new package, specify the package name and any additional parameters.

>[!tip] Best Practices for Model Management
- **Use Extensions Over Overlays**: Favor creating extensions rather than modifying existing elements directly to maintain compatibility with updates.
- **Clear Naming Conventions**: Use descriptive names for models to clarify their purpose and contents.

>[!attention] Advanced Considerations
- **Reference Models**: When creating a new model, carefully select which existing models to reference to manage dependencies effectively.
- **Deployment**: Consider how the model will be compiled into a deployable package, especially if it's in its own package, to streamline deployment processes.

#### Updating Model Parameters

>[!info] Modifying a Model
- Navigate to Dynamics 365 menu > Model Management > Update model parameters.
- Select the model to modify and adjust parameters such as dependencies and characteristics to align with project requirements.