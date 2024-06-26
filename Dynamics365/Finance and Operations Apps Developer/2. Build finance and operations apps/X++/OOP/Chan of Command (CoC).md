>[!summary]
>Chain of Command (CoC) is a powerful feature in Dynamics 365 for Finance and Operations that allows developers to extend the functionality of existing classes without modifying the original code directly, enhancing maintainability and upgradeability.

#### Definitions
- **Chain of Command (CoC)**: A design pattern used in X++ to extend the functionality of methods in a base class by wrapping additional logic around them.

>[!info] Implementing CoC
- **Extension Classes**: To apply CoC, create an extension class for the existing class, appending `_Extension` to the original class name.
- **Method Wrapping**: In the extension class, redeclare the method you want to extend and use the `next` keyword to call the original method as part of the execution chain.

>[!bug] Limitations in CoC
- Not all methods can be extended using CoC. Methods marked with `[Hookable(false)]`, `[Wrappable(false)]`, or `final` are not extensible.

>[!info] Steps to Use CoC
1. **Class Declaration**:
   - Use `[ExtensionOf]` to specify the base class.
   - Declare the class as `final` to prevent further inheritance.
   - Example:
     ```x++
     [ExtensionOf(classStr(ExampleClass))]
     final class ExampleClass_Extension
     {
         str doSomething(int arg)
         {
             // Custom logic before standard code
             var s = next doSomething(arg);
             // Custom logic after standard code
             return s;
         }
     }
     ```

>[!tip] Best Practices for Using CoC
- Place custom logic both before and after the `next` call within extended methods to ensure that your enhancements integrate smoothly with the base functionality.
- Regularly review and test the extended methods to ensure they behave as expected when updates are made to the base class.

>[!example] Practical Application of CoC
- **Scenario**: Extending a method to include validation checks before executing the base logic and logging information afterward.
  - This approach allows developers to inject custom validation rules and logging without disrupting the core business logic provided by the base application.

>[!attention] Advanced Considerations
- **Performance Impact**: Overusing CoC can impact performance. Monitor the execution time of methods using CoC, especially in performance-critical applications.
- **Debugging**: Debugging can be more complex in systems heavily utilizing CoC due to the multiple layers of method calls.
