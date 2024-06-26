>[!summary]
>Interfaces in X++ define contracts for class behaviors without dictating how those behaviors are implemented, allowing different classes to share the same interface but behave differently.

#### Definitions
- **Interface**: A contract that defines a set of public methods without implementing them. It specifies what a class must do, not how.

>[!info] Creating and Implementing Interfaces
- **Creation**: Define an interface in Visual Studio by adding a new interface item to your project.
- **Implementation**: Use the `implements` keyword in a class to adopt and define the methods outlined in an interface.

>[!bug] Common Pitfalls
- Failing to implement all interface methods in a class can lead to compilation errors.
- Interfaces must be public and their methods must also be explicitly declared as public in the implementing class.

>[!info] Steps to Implement an Interface
1. **Define the Interface**:
   ```x++
   public interface IDrivable
   {
       int getSpeed();
       void setSpeed(int newSpeed);
   }
   ```
2. **Implement the Interface in a Class**:
   ```x++
   class Automobile implements IDrivable
   {
       int m_speed;

       public int getSpeed()
       {
           return m_speed;
       }

       public void setSpeed(int newSpeed)
       {
           m_speed = newSpeed;
       }
   }
   ```

>[!tip] Best Practices for Using Interfaces
- Clearly define interface methods to ensure they are universally applicable to all potential implementing classes.
- Use interfaces to enforce consistency across different classes that share common functionalities.

>[!example] Practical Usage of Interfaces
- **Testing Interface Implementation**:
  ```x++
  class UseAnAutomobile
  {
      void DriveAutomobile()
      {
          IDrivable yourIDrivable;
          Automobile myAutomobile = new Automobile();

          if (myAutomobile is IDrivable)
          {
              yourIDrivable = myAutomobile;
              yourIDrivable.setSpeed(42);
              Global::info(int2str(yourIDrivable.getSpeed()));
          }
      }
  }
  ```
- This example checks if `Automobile` implements `IDrivable` and uses its methods to set and retrieve speed.

>[!attention] Advanced Interface Concepts
- **Multiple Interfaces**: A class can implement multiple interfaces, separating each interface name with commas.
- **Interface Extension**: An interface can extend another interface using the `extends` keyword, but it cannot extend more than one.