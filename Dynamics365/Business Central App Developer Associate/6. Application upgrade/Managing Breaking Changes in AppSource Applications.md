>[!summary] 
To manage breaking changes in [[AppSource]] applications, developers should use tools like AppSourceCop, hide internal implementations, compile against the latest dependencies, and announce upcoming breaks using deprecation properties.

#### Definitions
- **Breaking Change**: A modification requiring updates to the application to maintain integration, perceived as disruptive but necessary for progress.

>[!info] Techniques to Handle Breaking Changes
- **AppSourceCop**: An analyzer to detect and enforce rules against breaking changes.
- **Hide Internal Implementations**: Prevents dependencies on implementation details.
- **Compile Regularly**: Ensures compatibility with the latest dependencies.
- **Deprecation Properties**: Notify users of upcoming breaking changes.

>[!info] Properties of Breaking Changes
- Destructive to your solution.
- Requires work to fix.
- Perceived as an annoyance.
- Necessary for innovation.

>[!info] Documentation
- AppSourceCop Analyzer Rules document code changes considered breaking. The list evolves over time, and issues can be reported for new rules.

>[!tip] Avoiding Breaking Changes
- Maintain existing public APIs.
- New public APIs should coexist with old ones.
- Hide implementation details to prevent dependencies.

>[!tip] Techniques for Code Coexistence
1. **Versioning**: Manage different versions of APIs.
2. **Product Switches**: Enable or disable new functionality as needed.
3. **Syncing**: Ensure both old and new implementations work simultaneously.
4. **Rerouting**: Redirect old functionality through new implementations or overload with new features.

>[!info] Guidelines for Code Coexistence
- **Switches**: Either the old or new implementation works, not both.
- **Syncing**: Both implementations work, but can be complex to implement.

>[!info] Hiding Implementation Details
- **Access Property**: Control the accessibility of methods and properties.
- **Extensible Property**: Allow for future extensions without exposing implementation details.

>[!example] Introducing Breaking Changes Correctly
- Use the following properties in AL to manage deprecation:
  - **ObsoleteState**: Indicates the status of the deprecation.
  - **ObsoleteReason**: Explains why the element is deprecated.
  - **ObsoleteTag**: Provides additional context or tags related to the deprecation.

>[!info] Microsoft's Approach to Breaking Changes
- Microsoft aims to notify users of breaking changes in advance.
- Breaking changes are documented in the code.
- Non-breaking changes or critical issues may be addressed without prior notice.