>[!summary]
>Workflows in [[Business Central]] connect business-process tasks across different users, including system tasks like automatic posting. They streamline processes such as document approvals, notifications, and integration actions.

#### Workflow Uses in [[Business Central]]
- **Approve Sales and Purchase Documents:** Submit documents for approval according to a predefined hierarchy.
- **Approve Items, Customers, or Vendors:** Require approval for new entries or changes to critical fields.
- **Notify Users:** Inform users about creation or changes of items, customers, or vendors.
- **Integration Workflows:** Automate actions for incoming documents, such as sending them to an OCR service.

#### Setting Up and Using Workflows
- **Setup:** Enable workflows, configure workflow users, and specify notification methods.
- **Creation Methods:**
  1. **Manual Creation:** Create workflows from scratch.
  2. **From Template:** Copy and adjust predefined workflow templates.
  3. **Copy Workflow:** Duplicate an existing workflow.
  4. **Import from File:** Import workflows from another Business Central database.

>[!info] Workflow Setup Steps
1. **Enable Workflows:** Navigate to the workflow setup area in Business Central.
2. **Configure Users:** Assign workflow roles and permissions to relevant users.
3. **Specify Notifications:** Determine how users will receive workflow-related notifications (e.g., email, in-app).

>[!example] Approve Sales Document Workflow
- **Scenario:** Approving a sales quote.
  1. Salesperson submits the quote.
  2. Workflow sends the quote to the approval manager.
  3. Approval manager reviews and approves/rejects the quote.
  4. If approved, the system posts the quote automatically.

#### Practical Use Cases
- **Approval Hierarchy:** Define approval levels based on document types and approval limits.
- **Custom Notifications:** Set up alerts for changes in critical data fields without requiring approval.
- **Integration Actions:** Automatically process incoming documents through third-party services like OCR.
