>[!summary]
>Building a Software Deployable Package (SDP) from Visual Studio for Dynamics 365 involves using Azure DevOps to queue builds and manage the deployment of code changes to non-development environments.

#### Definitions
- **Software Deployable Package (SDP)**: A compiled package of application models that can be deployed to various Dynamics 365 environments.
- **Azure DevOps**: A suite of development tools used for building, testing, and deploying software.

>[!info] Building SDPs in Visual Studio

To deploy updates or customizations to your Dynamics 365 environment, create an SDP by queuing a build in Azure DevOps directly from Visual Studio.

>[!bug] Build Queue Challenges

Ensure all necessary parameters are set correctly when queuing the build to avoid failures or incorrect configurations.

>[!info] Steps to Build an SDP

1. Open Team Explorer in Visual Studio.
2. Navigate to the Builds section and right-click your build definition.
3. Select "Queue New Build" and confirm parameters in the build queue dialog box.
4. Monitor the build process and download the deployable package upon completion.

>[!tip] Monitoring Builds

Use the Team Explorer's My Builds section to track the progress of your builds, helping you identify and address issues promptly.

>[!attention] Handling Build Artifacts

After a build completes:
- Download the AX Deployable Runtime (SDP) from the Artifacts section of the build’s detail page on Azure DevOps.
- Upload the SDP to the Lifecycle Services Asset Library for deployment.

>[!example] Efficient Build Management

Ensure continuous integration and deployment by regularly updating build parameters and keeping your Azure DevOps pipeline aligned with your project’s requirements. This ensures that each build is relevant and ready for deployment.

>[!info] Integration with Lifecycle Services

After successfully building the SDP, uploading it to the Lifecycle Services Asset Library facilitates controlled and traceable deployments, essential for maintaining system integrity and supporting audit processes.