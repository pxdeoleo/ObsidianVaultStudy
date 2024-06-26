>[!summary]
>Scope and access modifiers in X++ dictate where variables and methods can be accessed within the codebase, impacting encapsulation, security, and inheritance.

#### Definitions
- **Scope**: The region of the code where a variable or method is accessible.
- **Access Modifiers**: Keywords that define how methods and variables can be accessed in relation to other parts of the code.

>[!info] Types of Access Modifiers
1. **Public**: Accessible from any class, allowing overriding unless marked as `final`.
2. **Protected**: Accessible within the class and its subclasses but not outside.
3. **Private**: Restricted to the class where it's declared, cannot be overridden.
4. **Internal**: Accessible only within the same model, similar to internal in C#.

>[!bug] Common Scope Issues
- Incorrect usage of access modifiers can lead to unintended data exposure or restrict necessary access.

>[!info] Variable Scopes
- **Instance Variables**: Declared within a class but outside methods; accessible in all methods of the class or subclasses if public or protected.
- **Local Variables**: Declared within methods and accessible only within the same method.
- **Parameters**: Act like local variables but are initialized with values passed during method invocation.

>[!tip] Best Practices for Managing Scope
- Use the most restrictive access necessary to safeguard class internals and prevent unintended interactions.
- Clearly define variable scopes to enhance code readability and maintainability.

>[!example] Demonstrating Scope and Access Modifiers
- **Class and Method Definitions**:
  ```x++
  internal class MyInternalClass
  {
      internal void myInternalMethod() { }
  }

  class Test
  {
      str a = "Car";
      int b = 20;
      str c;
      int d;

      public void method1(str x, int y)
      {
          c = x;
          d = y;
      }
  }
  ```
- **Parameter Passing and Local Variables**:
  ```x++
  class InfoValue
  {
      void method1(int a)
      {
          a = a + 1; // Local increment
          info(int2str(a)); // Displays 6
      }

      void method2()
      {
          int a = 5;
          info(int2str(a)); // Displays 5
          this.method1(a);
          info(int2str(a)); // Still displays 5, proving call by value
      }
  }
  ```

>[!attention] Understanding Call by Value vs. Call by Reference
- In X++, variables passed as parameters are typically handled by value, meaning changes made to the parameter inside the method do not affect the original variable.