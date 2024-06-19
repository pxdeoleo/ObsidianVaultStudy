**1. Role of Source Control:**

- **Purpose:** Tracks code changes and manages contributions from multiple developers.
- **Tools:** Azure DevOps, accessible via web browser or Visual Studio's Team Explorer.

**2. Azure DevOps Overview:**

- **Service Type:** Cloud-based source control with a 99.9% SLA.
- **Benefits:** Immediate access to new features, improved connectivity, simplified management.
- **Integration:** Replaces Team Foundation Services for Dynamics AX upgrades.

**3. Setting Up Azure DevOps:**

- **Account Creation:** Sign up at [Visual Studio Website](https://visualstudio.microsoft.com/), choose a URL for your account.
- **Project Setup:** Create a new project after setting up an account.

**4. [[Configuring Visual Studio for Azure DevOps]]:**

- **Connection Setup:**
    - Open Visual Studio as administrator.
    - Navigate to Team Explorer > Manage Connections > Connect to Team Project.
    - Add the Azure DevOps project URL and connect to the selected project.
- **Workspace Mapping:**
    - Use Source Control Explorer to map Azure DevOps project to local folders.
    - Map Metadata and Projects folders to specific local directories for synchronization.

**5. Managing Projects in Azure DevOps:**

- **Source Control on New Projects:**
    - Enable "Add to Source Control" during new project creation in Visual Studio.
- **Check-In Process:**
    - Commit changes to create new versions, allowing visibility and traceability of modifications.
    - Enables reverting to previous versions if needed.