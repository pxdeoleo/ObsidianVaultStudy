>[!summary]
>Understanding structured programming constructs in X++ is crucial for developers working with Dynamics 365. This note explores the use of classes, methods, and variables in X++ programming.

#### Definitions
- **Class**: A blueprint for creating objects which encapsulates data for the object and methods to manipulate that data.
- **Method**: Functions defined inside a class that dictate the behavior of objects.

>[!info] Class Components
- **Variables**: Stored in classes, these represent the state of an object and can have different access levels.
- **Methods**: Defined actions that an object can perform.

>[!bug] Common Misunderstandings
- Confusion can arise regarding the visibility of class members if modifiers are not explicitly used. Best practice is to always declare visibility to avoid ambiguity.

>[!info] Visibility Modifiers
- **Private**: Accessible only within the class.
- **Protected**: Accessible within the class and its subclasses.
- **Public**: Accessible from any location.

>[!tip] Class Instantiation
- Objects must be instantiated from classes using the `new` keyword to utilize non-static methods.

>[!example] Class Usage in X++
- **Class Definition**:
  ```x++
  public class CustomerDetails
  {
      private str custName;
  }
  ```
- **Instantiation and Method Usage**:
  ```x++
  public class Truck
  {
      public TruckLoad createNewTruckLoad()
      {
          TruckLoad myTruckLoad = new TruckLoad();
          return myTruckLoad;
      }
      public void shipTruckLoad(TruckLoad _truckLoad)
      {
          _truckLoad.ship();
      }
      public static int calcTotalWeight(int netWeight, int tareWeight)
      {
          return netWeight + tareWeight;
      }
  }
  ```

>[!attention] Method Types
- **Instance Methods**: Require an instance of the class to be called.
- **Static Methods**: Do not require an instance and can be called directly using the class name.

>[!info] Method Structure
- Methods include a signature (return type, name, parameters) and a body, which contains the executable code.
- Parameters should be prefixed with `_` to differentiate them from local variables.
