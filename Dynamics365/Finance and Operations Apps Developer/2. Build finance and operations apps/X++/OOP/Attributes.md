>[!summary]
>Attributes in X++ provide a powerful way to add metadata to classes and methods, influencing how they behave during compilation and runtime. This note explores how to apply and create custom attributes.

#### Definitions
- **Attribute**: A metadata element used to control the behavior of code elements such as classes and methods by providing additional information to the compiler or runtime environment.

>[!info] Applying Attributes
- Attributes are applied by placing them in square brackets above the declaration of the class or method.
- Example Usage: `SysObsoleteAttribute` can deprecate code elements, displaying warnings or errors during compilation.

>[!bug] Common Misuses of Attributes
- Incorrectly configuring attribute parameters can lead to unexpected behavior or compile-time errors.

>[!info] Creating Custom Attributes
- **Extend SysAttribute**: To create a custom attribute, extend `SysAttribute` and define any necessary fields and constructors.
- **Example Definition**:
  ```x++
  public class PracticeAttribute extends SysAttribute
  {
      StartEnd startEndEnum;
      str reason;

      public void new(StartEnd _startEndEnum, str _reason)
      {
          startEndEnum = _startEndEnum;
          reason = _reason;
      }
  }
  ```

>[!tip] Best Practices for Attribute Use
- Clearly document the purpose and parameters of custom attributes to ensure they are used correctly.
- Utilize attributes to enforce coding standards, enhance security, and manage compatibility.

>[!example] Practical Application of Attributes
- **Decorating Classes and Methods**:
  ```x++
  [PracticeAttribute(StartEnd::End, "Use the RegularClass class at the end.")]
  public class RegularClass
  {
      [PracticeAttribute(StartEnd::Start, "Use the rehearse method at the start.")]
      public int rehearse()
      {
          int rehearseValue;
          return rehearseValue;
      }
  }
  ```
- **Use Cases**:
  - Web services: `WebMethod` attribute makes a method callable over SOAP.
  - Interoperability: `DLLImportAttribute` for invoking unmanaged code.
  - Serialization: Attributes that define how classes and members map to XML nodes.

>[!attention] Advanced Use Cases
- Attributes can define how methods interact with security protocols, influence serialization processes, and provide versioning and compatibility information.
