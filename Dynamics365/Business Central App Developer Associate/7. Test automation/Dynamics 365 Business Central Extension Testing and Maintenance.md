> [!summary] 
> Key points for testing Dynamics 365 Business Central Extensions to ensure error-free deployment and smooth user experience.

#### Definitions

- **Dynamics 365 Business Central**: A business management solution for small and mid-sized organizations.
- **Docker**: A platform for developing, shipping, and running applications in containers.
- **CRONUS Demo Data**: Standard evaluation demo data used by Microsoft for app validation.

> [!info] Environment Testing

- Always test in a Dynamics 365 Business Central online environment to catch errors not seen in on-premises deployments.
- Use Docker for development and testing to match the validation environment used by Microsoft.

> [!bug] Common Errors to Avoid

- Ensure the extension publishes without code signing errors; do not use the skipverification flag.
- Verify the extension installs, uninstalls, and republishes without errors.

> [!info] Assisted Setup

- Ensure Assisted Setup wizards complete without errors.
- Test as a non-SUPER user to catch permission-related issues.

> [!info] Setup and Usage

- Walk through setup and usage of the extension to ensure functionality.
- Use the correct Docker image tag from the Collaborate site to set up the current Dynamics 365 Business Central version.

> [!info] CRONUS Demo Data

To use the correct demo data:

1. Search for Configuration Packages and select the link.
2. Choose Process > Import Predefined Package.
3. Click the link for GB.ENU.EVALUATION and start processing.
4. Apply the package and sign out, then back in.

> [!tip] User Permissions for Testing

- Do not test with a SUPER user; use a user with BUS FULL ACCESS permission set and your own permission sets.

> [!info] Thorough Testing

- Test 100% of the app functionality to ensure no permission errors.
- Microsoft expects developers to perform complete testing.

> [!attention] Continuous Maintenance

- Regularly test against the release branch in the Collaborate program to catch changes that may impact the app.
- Perform thorough testing against the monthly service updates and the major release branch.