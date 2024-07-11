> Developing applications for Microsoft Dynamics 365 [[Business Central]] with [[Visual Studio Code for Business Central|Visual Studio Code]] requires the AL Language extension. Install it via the Visual Studio Code Marketplace. Microsoft offers three methods to test and debug applications: online cloud sandbox, Docker images, and on-premises versions.

#### Steps to Install AL Language Extension

1. Open the Extensions tab in Visual Studio Code (fifth tab on Activity Bar or Ctrl+Shift+X).
2. Search for "AL Language" in the Marketplace.
3. Click the green Install button.

> [!info] Testing and Debugging

- **Online Cloud Sandbox**: Most current version.
- **Docker Images**: Versions based on cloud sandbox or on-premises.
- **On-Premises**: Local environment.

> [!info] Docker Images

- Obtain Docker images through Microsoft Collaborate.
- Includes updated AL Language Extension with new features.
- Download and install the VSIX file from the Docker image.

> [!tip] Installing VSIX Files

1. Open the Extensions tab (Ctrl+Shift+X).
2. Disable AL Language Extension from the Marketplace.
3. Click the ellipsis (...) above the Search Extensions field.
4. Select "Install from VSIX..." and install the downloaded file.

> [!info] Prerelease Versions

- Available via the existing Visual Studio Code mechanism.
- Visit the Prerelease Extensions documentation for details.
- Use the drop-down list to install or switch to prerelease versions.

#### Tags

#VSCode #BusinessCentral #ALLanguage #Extensions #Development #MicrosoftDynamics #Docker #Testing