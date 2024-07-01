>[!summary]
>Forms in Dynamics 365 Finance and Operations are essential for data entry and display. They utilize a variety of methods to handle user interactions, data initialization, validation, and updates. Extending these methods allows customization without altering base code.

#### Definitions
- **Form Methods**: Functions associated with form events like opening, closing, or updating a form.

>[!info] Standard Form Methods Overview

Form methods are divided into two categories:
- **Standard Methods**: Provided by the system, used for initialization and control handling.
- **Custom Methods**: Developer-defined for specialized behavior.

>[!bug] Importance of Super() Call

Always include a `super()` call in overridden methods to ensure that the base class behavior is executed, maintaining the integrity of form operations.

>[!info] Key Form Methods

1. **Init()**: Initializes the form. Commonly used to set up data sources or UI elements based on parameters.
2. **Close()**: Handles actions when a form is closed.
3. **Run()**: Executes after `init()` to prepare the form for user interaction.

>[!tip] Best Practices for Method Extension

Use the Chain of Command (CoC) to extend form methods safely. This approach allows you to add or modify form behavior without modifying the original codebase directly.

>[!attention] Handling Data Source Methods

Form data sources also have standard methods like:
- **Init()**: Prepares the data source when the form is loaded.
- **ValidateWrite()**: Ensures data integrity before saving to the database.
- **Active()**: Called when navigating between records in a form.

>[!example] Customizing Data Source Methods

Here’s how to customize the `active()` method to conditionally enable form fields:

```X++
[DataSource]
class TrainingMaster
{
    public int active()
    {
        int ret = super();
        this.formRun().controlMethodEnable(fieldNum(TrainingMaster, Venue),
            this.TrainingType != TrainingType::Online);
        return ret;
    }
}
```

This example checks the training type and conditionally enables the `Venue` field.

>[!info] Extending Form Controls

Chain of Command can also be used to extend control event handlers. For instance, you can customize the behavior of a button click without altering the original form's code.

>[!example] Extending a Button Click Event

```X++
[ExtensionOf(formControlStr(CustTable, updateButton))]
final class UpdateButton_Extension
{
    public void clicked()
    {
        // Custom code before the base call
        next clicked(); // Ensures the original button functionality is preserved
        // Custom code after the base call
    }
}
```

This approach ensures that you can add functionality around the original button click behavior without losing or overriding the base functionality.

>[!info] Ensuring Form Usability

While extending forms, ensure all modifications are tested in a controlled environment to avoid disrupting the user experience. Maintain consistency with the application's design language to ensure a seamless user experience.