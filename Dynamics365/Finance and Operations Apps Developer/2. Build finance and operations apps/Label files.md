>[!summary]
>Creating and using label files in Microsoft Visual Studio allows for effective localization of user interfaces in Dynamics 365, supporting multiple languages and ensuring clarity and usability across global implementations.

#### Definitions
- Label Files: Files used in Dynamics 365 development to store text for UI elements in multiple languages, facilitating localization and internationalization.

>[!info] Creating Label Files

Label files are essential for storing UI text such as properties, information messages, warnings, and errors. These files should be created with clear naming conventions and structured appropriately for each language needed.

>[!bug] Modifying Standard Labels

Avoid altering standard labels provided by Microsoft; instead, create customized labels to ensure upgrades and maintenance do not overwrite your modifications.

>[!info] Process of Adding Label Files

To add a label file to a project:
1. In Solution Explorer, right-click the project and select Add > New Item.
2. Choose Label and Resources, then Label file to initiate the Label file Wizard.
3. Follow the wizard steps to specify Label file ID and select languages.

>[!tip] Label Management Best Practices

When creating labels, use descriptive and clear identifiers (Label IDs) that reflect their purpose and ensure they are easy to manage and reference within the code.

>[!attention] Building Label Files

Remember to build your label files after creation or modification to ensure they are correctly compiled and available for use in your application.

>[!example] Using Labels in Development

1. **Add Labels**: Open a label file in the designer, click New, and define the Label ID and text.
2. **Reference Labels in UI**: Use the label by referencing its ID in the properties of UI elements or within X++ code like this: `@MyLabelFile:CustName`.
3. **Manage Multilingual Labels**: For multiple languages, create corresponding labels in each language-specific label file.

>[!info] Extending and Customizing Labels

While you cannot extend labels directly, you can create new labels with the same ID but different text in a custom label file, allowing you to override the default text with your version without altering the original label file.

This approach enables tailored localization strategies while maintaining compliance with standard software practices, ensuring that applications meet diverse user needs and comply with global standards.