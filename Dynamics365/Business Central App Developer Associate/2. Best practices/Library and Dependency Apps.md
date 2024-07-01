>[!summary]
>Library and dependency apps streamline code management in Dynamics 365 Business Central by sharing common code across multiple applications. Understanding their installation and management is crucial for effective application development and maintenance.

#### Definitions
- **Library App**: A non-visible app that contains shared code used by other apps, which is automatically managed and installed by Business Central.
- **Dependency App**: Similar to a library app but listed on AppSource, requiring the installation of another app it depends on.

>[!info] Role of Library Apps
- Serve as a central repository for common code that multiple AppSource apps can utilize, enhancing maintainability and consistency.

>[!bug] Challenges with Update Mechanisms
- Current systems do not automatically update library apps when the main app is updated, potentially leading to compatibility issues.

>[!info] Installation Process
- Library apps are installed automatically and invisibly when a related AppSource app is installed, ensuring all dependencies are met without user intervention.

>[!tip] Managing Dependency Apps
- Clearly define and manage dependency relationships in the app's JSON manifest to ensure proper installation order and functionality.

>[!attention] Visibility and Access
- Unlike dependency apps, library apps do not appear on AppSource and are managed entirely within the Business Central environment.

>[!example] Scenario: Installing an App with Dependencies
1. A customer selects an app on AppSource.
2. Business Central checks the app’s JSON manifest for any library or dependency apps.
3. Required library and dependency apps are installed first, followed by the main app.

>[!info] Multiple Library Apps
- You can associate multiple library apps with a single AppSource app by listing them in the JSON manifest as dependencies.

>[!info] Future Developments
- Anticipate potential changes in how Business Central handles library and dependency updates, which may include automatic updates in future releases.