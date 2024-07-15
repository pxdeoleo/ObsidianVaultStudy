>[!summary]
In [[Business Central]], actions can be defined in AL code within a page’s layout section, under specific areas corresponding to menus in the command bar. Promoted actions can be used for quick access and organized using split buttons.

#### Definitions
- **Navigation Bar:** Top section with RoleCenter actions.
- **Command Bar:** Below navigation bar, actions defined on Card or List page.
- **Promoted Actions:** Actions pushed to the first part of the command bar for quick access.

>[!info] Action Areas
- **Navigation:** Navigate menu.
- **Creation:** New Document menu.
- **Reporting:** Report menu.
- **Processing:** Process menu.

Actions are defined within these areas under the layout section in AL code.

>[!info] Promoting Actions
- **Promoted Property:** Used to push actions to the command bar’s first part.
- **PromotedCategory:** Specifies the menu for the promoted action (e.g., New, Process).
- **PromotedIsBig:** Makes the action appear before others.
- **PromotedOnly:** Hides the action in other menus, only showing it in the promoted category.

>[!example] Defining Actions in AL
```al
page 50105 ActionRefPage
{
    actions
    {
        area(Promoted)
        {
            actionref(MyPromotedActionRef; MyBaseAction) { }
            group(Group1)
            {
                actionref(MySecondPromotedActionRef; MyBaseAction) { }
            }
            group(Group2)
            {
                ShowAs = SplitButton;
                actionref(MySplitButtonPromotedActionRef; MyBaseAction) { }
                actionref(MyOtherSplitButtonPromotedActionRef; MyBaseAction) { }
            }
        }
        area(Processing)
        {
            action(MyBaseAction)
            {
                Visible = true;
                trigger OnAction()
                begin
                    Message('Hello world!');
                end;
            }
        }
    }
}
```

>[!attention] New Promoted Actions Syntax
- Legacy and new syntax for promoted actions cannot be mixed on the same page.
- New syntax improves visibility and personalization options.

>[!info] Custom Actions
Custom actions can invoke external targets like Power Automate flows using specific properties:
```al
customaction(MyFlowAction)
{
    CustomActionType = Flow;
    FlowId = '<the-GUID-identifying-the-Power-Automate-Flow>';
    FlowEnvironmentId = '<the-GUID-identifying-the-Power-Automate-environment>';
}
```

#### Tags
#businesscentral #alcode #promotedactions #customactions #commandbar #development