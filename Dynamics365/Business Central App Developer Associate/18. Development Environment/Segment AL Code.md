> [!summary]
> Namespaces in AL help organize code into logical groups and hierarchies, preventing naming conflicts and enhancing code structure. An AL file can declare a namespace, and all objects in the file belong to that namespace. The same namespace can be used across multiple files, facilitating logical grouping and reuse.

#### Declaring Namespaces
- **Syntax**: `namespace MyNamespace;`
- Objects declared in the file belong to `MyNamespace`.
- Use the same namespace declaration in other files for grouping.

> [!info] Namespace Rules
- **Uniqueness**: Ensure global uniqueness.
- **Structure**: Use organization/product name followed by logical grouping.
  - Example: `namespace BigCompany.SmartProduct.SomeProductArea;`
- **Stability**: Avoid version-specific names; changing namespace is a breaking change.
- **Valid AL Identifier**: Namespace names can contain dots for hierarchy.

> [!tip] Using Directive
- Simplifies references to objects in other namespaces without fully qualified names.
- **Syntax**: 
  ```AL
  namespace MyNamespace;
  using SomeOtherNamespace;
  codeunit 10 MyCode { ... }
  ```

> [!info] Nested Namespaces
- **Syntax**: `namespace MyNamespace.MyNestedNamespace;`
- Use the fully qualified name or `using` directive to access nested namespaces.
- **Example**:
  ```AL
  namespace MyNamespace.MyNestedNamespace;
  using MyNamespace.MyNestedNamespace;
  ```

#### Best Practices
1. **Unique Names**: Ensure namespace uniqueness to avoid conflicts.
2. **Logical Grouping**: Use namespaces to group related functionality logically.
3. **Stable Names**: Choose stable, non-version-specific names.
4. **Using Directives**: Utilize `using` directives for simpler code references.

#### Benefits
- **Prevents Naming Conflicts**: Ensures unique object names.
- **Improves Structure**: Logical grouping of related code.
- **Enhances Navigation**: Easier to navigate and understand the codebase.
- **Facilitates Reuse**: Namespaces can be reused across multiple files.

#### Example Namespace Declaration
```AL
namespace BigCompany.SmartProduct.SomeProductArea;
// codeunits, tables, pages....
```

#### [[AL Explorer]]
- Shows namespaces for objects, allowing grouping by namespace.
- Enhances discovery and focus on app subareas.
- Identifies inconsistencies when adding new objects.

#### Tags
#BusinessCentral #Namespaces #ALCode #Development #MicrosoftDynamics #LogicalGrouping #CodeOrganization #ALExplorer