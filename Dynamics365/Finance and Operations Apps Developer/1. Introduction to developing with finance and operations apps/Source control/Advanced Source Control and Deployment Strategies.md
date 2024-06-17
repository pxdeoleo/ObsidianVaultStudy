**1. Handling Code Conflicts:**

- **Conflict Resolution:** Use Visual Studio's Resolve Conflicts page to manage code discrepancies.
- **Merge Options:** Choose between automatic merges or manual selection of code changes.

**2. Branching and Merging:**

- **Purpose:** Isolates software assets to enhance parallel development.
- **Common Branches:** Development, Test, Production.
- **Strategy:** Development for ongoing work, Test for ready-to-test changes, Production for deployment-ready code.

**3. Deployable Package Creation and Deployment:**

- **Creation Process:**
    - Navigate: Dynamics 365 > Deploy > Create Deployment Package.
    - Configure packages and set the location for the deployable package.
- **[[Lifecycle Services]] Integration:**
    - Upload and manage packages through [[Lifecycle Services]] for deployment.

**4. Deployment Procedures:**

- **Nonproduction Environment:**
    - Update application through Environment details view > Maintain > Apply updates.
- **Production Environment:**
    - Schedule and deploy packages via [[Lifecycle Services]] with monitoring of deployment status and rollback options if necessary.

### Visual Aids:

- Screenshot of the New Project page in Visual Studio highlighting the "Add to Source Control" checkbox.
- Screenshots of the Azure DevOps setup and project configuration windows.
- Resolve Conflicts page layout showing different code comparison panes.

**Note:** These notes are structured to facilitate easy understanding and application of Azure DevOps for finance and operations app development.
