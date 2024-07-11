>[!summary]
>AL code for obtaining session and environment information to modify [[Business Central]] behavior in Teams. This includes determining if the session runs in Teams, if the user has only a Microsoft 365 license, and if Microsoft 365 collaboration is enabled.

#### Checking Session in Teams
- Use `CurrentClientType` method to check if the session runs in Teams.
- Example usage: Adjust visibility of actions based on client type.
```AL
if CurrentClientType = ClientType::Teams then
    // Specific actions for Teams
```

#### Checking Microsoft 365 License
- Prevents data writing and simplifies UI for Microsoft 365-only users.
- Use the following code snippet to determine if the user has only a Microsoft 365 license:
```AL
procedure IsM365PlanUserOnly(): Boolean
var
    PlanIds: Codeunit "Plan Ids";
    UsersInPlans: Query "Users In Plans";
    IsM365PlanUser: Boolean;
    DoesUserHaveOtherPlans: Boolean;
begin
    UsersInPlans.SetFilter(User_Security_ID, UserSecurityId());
    if not UsersInPlans.Open() then
        exit(false);
    while UsersInPlans.Read() do
        if (UsersInPlans.Plan_ID = PlanIds.GetMicrosoft365PlanId()) then
            IsM365PlanUser := true
        else
            DoesUserHaveOtherPlans := true;
    exit(IsM365PlanUser and (not DoesUserHaveOtherPlans));
end;
```

#### Enabling Microsoft 365 Collaboration
- Administrators can enable Microsoft 365 license access for collaboration in Business Central.
- Use the following code snippet to check if this feature is enabled in the current environment:
```AL
procedure IsM365CollaborationEnabled(): Boolean
begin
    if CanQueryGraph() then
        exit(GraphQuery.IsM365CollaborationEnabled());
    exit(false);
end;
```

#### Practical Applications
- **Session in Teams:** Adjust page content and behavior when running in Teams.
- **Microsoft 365 License:** Simplify UI and restrict data writing for Microsoft 365-only users.
- **Collaboration Enabled:** Ensure environment settings support Microsoft 365-based data sharing.