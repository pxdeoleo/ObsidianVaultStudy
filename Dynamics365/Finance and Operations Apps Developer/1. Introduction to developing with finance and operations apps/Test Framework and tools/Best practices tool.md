>[!summary]
>The Best Practices tool in Visual Studio helps maintain clean and uniform X++ code, facilitating easier upgrades and readability for future developers.

#### Definitions
- Best Practices: Guidelines and automated checks in Visual Studio to ensure code quality and compatibility with future upgrades.

>[!info] Enabling Best Practices Checks

Best practices can be configured and enabled within Visual Studio under Dynamics 365 options, allowing developers to customize checks per model.

>[!bug] Suppression of Checks

Care must be taken when suppressing best practice warnings to ensure that important code quality issues are not overlooked.

>[!info] Accessibility of Best Practices

The Best Practices settings are accessible via the Extensions menu, where specific models can be configured individually.

>[!tip] Comprehensive Code Checks

Utilize the command line to run extensive best practice checks across different elements and models, ensuring thorough coverage.

>[!attention] Modification of Suppressions

When editing best practice suppressions, ensure that justifications are meaningful and relevant to maintain the integrity of code standards.

>[!example] Running Best Practices Checks

1. Open Visual Studio and navigate to the Best Practices configuration under Dynamics 365 options.
2. Enable or disable best practices checks as needed for specific models.
3. Use command line options to run targeted checks:
   - For all forms in a module: `xppbp -module:FleetManagement form:*`
   - For specific elements: `xppbp -module:FleetManagement class:MyClass form:MyForm`
   - For all items in a model: `xppbp -module:FleetManagement -model:FleetManagement -all`
   - Output to log files: `xppbp -module:FleetManagement -all -xmllog=Log.xml -log=Log.txt`
4. Review the results in the Best Practices page or the specified log files.

>[!info] Managing Suppressions

Modify the suppression XML file to fine-tune the best practices checks based on project needs and justify each suppression clearly for future reference.