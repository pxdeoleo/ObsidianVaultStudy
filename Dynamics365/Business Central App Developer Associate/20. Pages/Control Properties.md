>[!summary]
Different controls in the system have distinct properties like NotBlank, ShowMandatory, UpdatePropagation, and ApplicationArea, which determine their behavior and visibility on pages.

#### Definitions
- **NotBlank**: Mandatory field/property at both field and control levels; throws an error if left blank.
- **ShowMandatory**: Visual indication (red asterisk) of a mandatory field without enforcing the requirement.
- **UpdatePropagation**: Defines update behavior between mainpage and subpage.
- **ApplicationArea**: Defines visibility and differentiation of user experiences based on tags.

>[!info] NotBlank and ShowMandatory
- **NotBlank**: Used on fields and controls; mandatory if set.
- **ShowMandatory**: Only visual indication; no error if blank.

![ShowMandatory Property Alert](screenshot_showmandatory_alert.png)

>[!info] UpdatePropagation
- **Subpage**: Only updates the subpage.
- **Both**: Updates both subpage and mainpage.

>[!info] ApplicationArea
- **Purpose**: Differentiates user experiences by showing/hiding controls.
- **Location**: Found on pages, fields, parts, and action controls.
- **Format**: Comma-separated list of application area tags.
- **Special Tags**:
  - **All**: Control always appears.
  - **Basic,Suite**: Specific areas.
- **[[Inheritance]]**: Inherits from parent page or report if not set on control.
- **Rules**: AS0062 and PTE0008 updated for default settings from parent object.
- **UsageCategory**: Required for search visibility.

>[!info] UsageCategory
- **Purpose**: Enables pages/reports to be searchable in "Tell me".
- **Settings**: Must be set to a value other than None to be discoverable.
- **AdditionalSearchTerms**: Adds keywords for improved searchability.
- **Example**: Creating a SimpleItemList page with specified UsageCategory and AdditionalSearchTerms.

```al
page 50210 SimpleItemList 
{ 
    PageType = List; 
    SourceTable = Item; 
    UsageCategory = Lists;
    AccessByPermission = page SimpleItemList = X;
    ApplicationArea = All;
    AdditionalSearchTerms = 'product, merchandise';

    layout 
    { 
        area(content) 
        { 
            group(General) 
            { 
                field("No.";"No.") {} 
                field(Name;Name) {} 
                field(Description;Description) {} 
            } 
        } 
    } 
}
```

#### Tags
#properties #controls #notblank #showmandatory #updatepropagation #applicationarea #usagecategory #dynamics365 #businesscentral