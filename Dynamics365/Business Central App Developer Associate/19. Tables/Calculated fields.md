> [!summary] 
> Calculated fields are dynamically computed fields in the [[Business Central]] database. They are defined using the FieldClass property with values Normal, FlowField, or FlowFilter.
>
#### Definitions
- **Calculated fields**: Fields whose values are computed rather than stored directly in the database.
- **FieldClass property**: Determines the type of field; can be Normal, FlowField, or FlowFilter.

> [!info] Normal Fields
- Default FieldClass value.
- Data is stored directly in the database.
- Most fields in the Business Central database are normal fields.

> [!info] FlowFields
- Data is not stored but calculated using a formula.
- Requires a calculation formula defined in the CalcFormula property.
- Formula types include Sum, Lookup, Count, Exist, Average, Min, and Max.

> [!info] FlowFilter
- Used in FlowField calculations.
- Holds a temporary value for filtering within the calculation formula.
- Allows end users to provide filter values dynamically.

> [!example] FlowField Calculation Formula Types
1. **Sum**: Computes the sum of a specified set in a table column (decimal).
2. **Lookup**: Retrieves a value from a column in another table (any).
3. **Count**: Counts records in a specified set in a table (integer).
4. **Exist**: Checks if any records exist in a specified set in a table (Boolean).
5. **Average**: Calculates the average value of a specified set in a table column (decimal).
6. **Min**: Finds the minimum value in a specified set in a table column (any).
7. **Max**: Finds the maximum value in a specified set in a table column (any).

#### Tags
#calculatedfields #FieldClass #FlowField #FlowFilter #BusinessCentral #database #formulas