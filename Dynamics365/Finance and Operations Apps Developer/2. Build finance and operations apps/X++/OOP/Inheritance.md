>[!summary]
>Inheritance and abstract classes are foundational concepts in object-oriented programming (OOP), enabling code reuse and the creation of polymorphic structures in X++.

#### Definitions
- **Inheritance**: A mechanism where a new class (subclass) inherits attributes and methods from an existing class (superclass).
- **Abstract Classes**: Classes that cannot be instantiated directly and must be extended by other classes.

>[!info] Concept of Inheritance
- Inheritance allows subclasses to inherit and extend functionalities of a superclass, facilitating code reusability and extension.
- Example Scenario: A `Vehicle` class serves as a superclass for `Car`, `Bus`, and `Truck` classes, each inheriting properties like speed, color, and gears.

>[!bug] Common Misconceptions
- Not all properties should be inherited; some should be unique to subclasses to avoid inappropriate behavior or security issues.

>[!info] Implementing Inheritance
- **Example**:
  ```x++
  class Vehicle
  {
      real height;
      real width;

      new(real _height, real _width)
      {
          height = _height;
          width = _width;
      }
  }

  class Car extends Vehicle
  {
      int numberOfPassengers;

      new(real _height, real _width, int _numberOfPassengers): super(_height, _width)
      {
          numberOfPassengers = _numberOfPassengers;
      }
  }
  ```

>[!tip] Using Abstract Classes
- Abstract classes define templates for subclasses and include abstract methods that subclasses must implement.
- Abstract classes and methods provide a structured approach to enforce certain functionalities in subclasses.

>[!example] Abstract Class Usage
- **Abstract Class Definition**:
  ```x++
  abstract class Vehicle
  {
      str owner;
      int age;

      void printInfo()
      {
          info(strFmt("%1, %2", owner, age));
      }

      abstract void operate();
  }

  class Car extends Vehicle
  {
      str model;

      override void printInfo()
      {
          info(strFmt("%1, %2, %3", owner, age, model));
      }

      override void operate()
      {
          info("Running");
      }
  }
  ```

>[!attention] Design Considerations
- Ensure abstract classes are used when there is a clear hierarchical model and subclasses are expected to have distinct implementations of the defined abstract methods.
