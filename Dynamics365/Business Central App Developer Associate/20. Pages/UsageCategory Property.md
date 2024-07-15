>[!summary]
When developing pages in an AL extension, setting the `UsageCategory` property allows users to search for pages. The property should be set appropriately depending on the page type.

#### Definitions
- **UsageCategory Property**: Determines the category under which a page can be searched.
- **ApplicationArea Property**: Specifies the functional area of the application the page is associated with.

>[!info] [[Page types|Page Types]]

- **Administration**: For pages used to manage system settings and configurations.
- **Documents**: For transaction-based pages.
- **History**: For pages showing historical data.
- **Lists**: For list-based pages that users need to search.
- **None**: For pages not intended to be searched directly, like Card pages.
- **ReportsAndAnalysis**: For pages related to reports and data analysis.
- **Tasks**: For task-based pages.

>[!example] UsageCategory in List Pages

For List pages, always set the `UsageCategory` property so users can search for these pages. Also, set the `ApplicationArea` property.

```al
page 50100 MyListPage
{
    PageType = List;
    UsageCategory = Lists;
    ApplicationArea = All;

    // Additional page configurations
}
```

>[!example] UsageCategory in Card Pages

For Card pages, set the `UsageCategory` property to `None` and remove the `ApplicationArea` property. Users should open Card pages through List pages.

```al
page 50101 MyCardPage
{
    PageType = Card;
    UsageCategory = None;

    // Additional page configurations
}
```

>[!tip] Searching for Pages

Use the search icon to find newly created pages. They will appear under the category specified by the `UsageCategory` property.
#### Tags
#AL #UsageCategory #ApplicationArea #ListPages #CardPages #BusinessCentral #Development