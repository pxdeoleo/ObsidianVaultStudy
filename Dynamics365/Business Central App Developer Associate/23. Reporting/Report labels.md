> [!summary] 
> Labels in [[Reports|report]] parameters are used for adding text fields such as report titles or custom text values, enhancing multilingual capabilities and performance.

#### Definitions
- **Labels**: Text fields added to report parameters for captions, titles, or custom text values.
- **Dataset**: Collection of data items used in report layouts.

> [!info] Adding Labels
- Labels can be related to data items (e.g., table field captions) or unrelated (e.g., report title).
- Labels must be included in the dataset for use in the report layout.

> [!tip] Multilingual Advantage
- Using labels allows text to be included in translation files, making the report multilingual.
- Hard-coded text values do not become part of translation files and aren't multilingual.

> [!info] Performance Impact
- Labels improve performance as they are added to the parameters of the layout, not the dataset.
- More fields in the dataset increase its size, negatively impacting report performance.

> [!example] Code Sample for Labels
```al
labels
{
  LabelName1 = 'Label Text1', Comment='Foo', MaxLength=999, Locked=true;
  LabelName2 = 'Label Text2', Comment='Foo', Locked=false;
}
```

> [!info] Usage in RDL and Word Layouts
- Labels are used in RDL and Word report layouts for field captions, chart titles, or report titles.

#### Tags
#reports #labels #performance #multilingual #dataset