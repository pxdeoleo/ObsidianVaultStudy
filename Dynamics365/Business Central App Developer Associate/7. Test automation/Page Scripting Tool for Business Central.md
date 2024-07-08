 > [!summary] 
 > The page scripting tool in Business Central records user interactions with the UI for automated replay, facilitating user acceptance testing (UAT) by eliminating manual test repetition.

#### Definitions

- **Page Scripting Tool**: A tool to record and replay user interactions within Business Central.
- **User Acceptance Testing (UAT)**: Testing to validate that a system meets user needs and requirements.

> [!info] Permissions Required

- **Recording**: Requires PAGESCRIPTING - REC permission set.
- **Playback**: Requires PAGESCRIPTING - PLAY permission set.

> [!info] Features

1. **Record Interactions**: Records UI actions and resulting code executions.
2. **Playback**: Replays recorded actions with real-time feedback.
3. **Session Information**: Access user session data for dynamic testing.
4. **Clipboard**: Copy and paste control values within the tool.
5. **Validation Steps**: Assert control values during playback.
6. **Conditional Steps**: Execute steps based on conditions.
7. **Wait Steps**: Add delays between steps for timing control.
8. **Optional Pages**: Handle pages that appear conditionally.

> [!example] Using the Page Scripting Tool

**Starting the Tool**:

1. Open from the role center or any page: **Settings > Page Scripting**.
2. Use the control bar in the Page Scripting pane to start, pause, or stop recording.

**Making a Recording**:

1. **Start Recording**: Open the desired page, select **Start new** or **New recording**.
2. **Perform Actions**: Interact with the application; actions are recorded sequentially.
3. **Pause/Resume**: Use the control bar to pause and resume recording.
4. **Edit Steps**: Delete or modify steps during recording.
5. **Save Recording**: Select **Save recording** to save for later use.

**Inserting Special Steps**:

1. **Copy/Paste**: Right-click a control, select **Page Scripting > Copy** or **Paste**.
2. **Validation**: Right-click, select **Page Scripting > Validate** to add validation steps.
3. **Conditional Steps**: Right-click, select **Page Scripting > Add conditional steps**.

**Playback**:

1. **Play**: Select **Play recording** to replay actions.
2. **Navigate**: Use control bar buttons to move steps forward/backward or rewind.
3. **Save Results**: Save playback results as a YAML file or share as a link.

#### Best Practices

1. **Start from Known Place**: Begin recording from a consistent starting point like the role center.
2. **Filter Grids**: Ensure desired values are easily selectable by filtering grids.
3. **Use New Entities**: Create new entities for tests to avoid data dependencies.
4. **Break Down Recordings**: Segment recordings into smaller, manageable parts.

**Examples**:

- **Recording 1**: Setup user.
- **Recording 2**: Create customer.
- **Recording 3**: Create sales order.
- **Recording 4**: Post sales order.

#### Additional Tips

- Avoid dependencies on unavailable data.
- Ensure the system state is consistent before and after tests.
- Validate steps using current values, clipboard values, or custom Power Fx expressions.
- Use optional pages for conditional flows in the UI.