>[!summary]
X++ supports primitive and composite data types. Primitive data types map to physical database types, enhancing data integrity and simplifying programming. Extended Data Types (EDTs) are recommended for use in development due to their readability and property inheritance.

#### Definitions

- **Primitive Data Types**: Basic types such as Booleans, Dates, Enums, GUIDs, Integers, Reals, Strings, TimeofDay, and UTCDateTime, directly mapped in the AOT.
- **Composite Data Types**: Include arrays, containers, classes, delegates, and tables, allowing for complex structures and data manipulation.
- **EDTs (Extended Data Types)**: User-defined types based on primitive types, enhancing code readability and consistency across the system.

> [!info] Benefits of Using EDTs

EDTs improve code readability, ensure property consistency, support hierarchy, and enhance user interface interactions such as lookups and drop-down lists. They are reusable across various application fields.

> [!example] Implementation in Visual Studio

In Visual Studio, create and manipulate EDTs within the AOT to define system-wide data fields and behaviors. Use properties to define display characteristics and control behaviors like lookups and validations.

**Key Takeaways**

- **Consistency**: EDTs ensure uniform properties across application instances.
- **Readability**: Meaningful names in EDTs improve code clarity and maintenance.
- **Flexibility**: Property inheritance from parent EDTs allows tailored data handling.