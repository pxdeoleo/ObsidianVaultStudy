>[!summary]
A workflow in Dynamics 365 [[Business Central]] consists of three components: Workflow Event, Workflow Condition, and Workflow Response.

#### Definitions
- **Workflow Event**: An action within the system that triggers a response.
- **Workflow Condition**: Moderates the workflow event specified in the When Event field, with predefined condition values.
- **Workflow Response**: Actions performed by the system when an event occurs that meets the predefined condition.

>[!example] Procedure to Create a Workflow

1. **Accessing [[Workflows]]**:
   - Select the search icon in the upper-right corner.
   - Enter "[[workflows]]" and select the related link.
2. **Creating a New Workflow**:
   - Select **New**.
   - **Code field**: Enter up to 20 characters to identify the workflow (e.g., `US-CUSTLIM_01`).
   - **Description field**: Enter `Notify on customer credit limit change`.
   - **Category field**: Select `SALES` from the lookup values.
3. **Defining Workflow Event**:
   - **When Event field**: Select `A customer record is changed` from the Workflow Events page.
4. **Setting Event Conditions**:
   - **On Condition field**: Set conditions relevant to the event. 
   - Example: Select the `Credit Limit ($)` field, choose `is Changed`.
5. **Defining Workflow Response**:
   - **Then Response field**: Select `Create a notification for %1`.
   - **Options for the Selected Response**:
     - **Notify Sender**: If selected, the requestor is notified instead of the recipient.
     - **Recipient User ID**: Specifies the user to receive the notification.
     - **Notification Entry Type**: Choose between record change, approval request, or past due date.
     - **Link Target Type**: Specifies another page in Business Central.
     - **Custom Link**: Add a URL link to the notification.
   - **Options for Creating an Approval Request**:
     - **Due Date Formula**: Days to resolve approval from the sent date.
     - **Delegate After**: Days after which the request is delegated.
     - **Approver Type**: Determines the approver based on setup.
       - **Approver Limit Type**: Specifies the creation of approval request entries:
         - **Approver Chain**: All approvers up to the first qualified.
         - **Direct Approver**: Immediate approver only.
         - **First Qualified Approver**: First qualified approver only.
   - **Options for Creating Journal Lines**:
     - **General Journal Template Name**: Name of the journal template.
     - **General Journal Batch Name**: Name of the journal batch.

6. **Activating the Workflow**:
   - Select the **Enabled** field to start using the workflow.

>[!tip] Organizing Workflow Steps

- **Indentation**:
  - Use **Increase Indent** and **Decrease Indent** buttons to define step positions.
  - **Next in Sequence**: Indent under the previous step's event name.
  - **Alternative Steps**: Place at the same indentation level; prioritize by order.
#### References
- Workflow Events, Workflow Conditions, and Workflow Responses are selected and configured on the Workflow page.
- Options and specific fields are available based on the type of workflow response chosen.
- Workflow setup involves defining user roles and notification parameters.
