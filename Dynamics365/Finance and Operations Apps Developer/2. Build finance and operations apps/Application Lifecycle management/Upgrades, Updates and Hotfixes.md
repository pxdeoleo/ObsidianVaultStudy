>[!summary]
>This note outlines the procedures for handling different types of system updates in Dynamics 365 for Finance and Operations, including upgrades from older versions, as well as applying updates and hotfixes to both cloud and on-premises environments.

#### Upgrade from Microsoft Dynamics AX 2012
- **Phases of Upgrade**:
  - **Analyze**: Assess the effort required for the upgrade and prepare a detailed project plan. Utilize reports provided during this phase for better project estimation.
  - **Execute**: Implement code and data upgrades identified during the analyze phase. Install necessary hotfixes on development machines.
  - **Validate**: Conduct final testing and create a cutover plan. This phase is crucial for ensuring that the system functions correctly before going live.

>[!info] Upgrade Resources
- For detailed instructions and resources on upgrading from Dynamics AX 2012, visit Microsoft Learn and search for the latest upgrade guides.

#### Apply Updates to On-premises Versions
- **Types of Updates**:
  - Platform binary updates
  - Application binary updates
  - Application X++ updates
- **Process**:
  - Updates are applied through deployable packages from Lifecycle Services.
  - Follow the guidelines in Lifecycle Services to generate and apply these packages to your on-premises environments.

#### Apply Updates to Cloud Versions
- **Procedure**:
  - For non-production environments, updates are manually initiated from the 'Maintain' section in Lifecycle Services.
  - For production and sandbox environments, continuous updates require pre-configuration of update settings in Lifecycle Services. This setup must be completed before the environment goes live to ensure smooth transitions during updates.

>[!bug] Common Issues
- Delays in update rollouts can occur if pre-update checks are not thoroughly conducted.
- Insufficient testing in non-production environments before applying updates to production can lead to unexpected disruptions.

#### Installing Hotfixes
- **Development Environment**:
  - Hotfixes should be regularly applied to development environments to address specific issues before they impact production systems.
  - Hotfix installation is part of the ongoing maintenance routine and should be scheduled during less critical operational periods to minimize disruption.

>[!tip] Best Practices for System Updates
- Always maintain a rigorous backup procedure before implementing any updates or hotfixes.
- Conduct thorough testing across all phases of updates to ensure compatibility and performance stability.
- Keep documentation of all changes and update procedures for audit purposes and operational continuity.

#### Validation and Testing
- **Cutover Testing**: Simulate the final move to production to catch any potential issues.
- **Functional Testing**: Verify that all aspects of the system operate as expected under the new update or after a hotfix is applied.