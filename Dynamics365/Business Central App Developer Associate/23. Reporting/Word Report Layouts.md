>[!summary]
Word report layouts in Microsoft Dynamics 365 Business Central use .docx templates to view and print reports. These layouts leverage custom XML parts in Word to map the dataset of a Business Central report. This guide explains how to develop Word report layouts using Microsoft Word 2016 or later.

#### Definitions
- **Word Report Layout:** A [[Built-in Report layouts|report layout]] based on a .docx file, utilizing Word's capabilities for design and printing.
- **Custom XML Part:** Structured XML in Word representing the dataset of a Business Central report.

>[!info] System Requirements
- Microsoft Word 2016 or later is required to develop Word report layouts.

>[!example] Example Report
```al
report 50100 ExampleWORDLayout
{
    Caption = 'ExampleWORDLayout';
    UsageCategory = ReportsAndAnalysis;
    ApplicationArea = All;
    DefaultRenderingLayout = ExampleWORDLayout;

    dataset
    {
        dataitem(Customer; Customer)
        {
            column(CustomerNo; "No.") { }
            column(CustomerName; Name) { }
            column(City; City) { }
            column(BalanceLCY; "Balance (LCY)") { }
        }
    }

    rendering
    {
        layout(ExampleWORDLayout)
        {
            Type = Word;
            LayoutFile = './src/Reports/WORD/ExampleWORDLayout.docx';
            Caption = 'ExampleWORDLayout';
            Summary = 'An example of a WORD Layout.';
        }
    }
}
```

>[!tip] Adding Layouts
- To enable multiple layouts, use the rendering section of a report object.
- Specify details like layout file path, caption, and summary in the layout section.

>[!example] Steps to Create Word Report Layout
1. **Set Up Word Layout:**
   - Open Visual Studio Code and build the extension (Ctrl+Shift+B) to generate the ExampleWORDLayout.docx file.
   - Right-click the generated file and select Open Externally.

2. **Edit in Microsoft Word:**
   - Enable the Developer tab (Options > Customize Ribbon > Developer).
   - Use the XML Mapping Pane to map the report dataset.
   - Insert a table with two rows and the necessary columns.
   - Set the second row as a repeater for dataset fields.

3. **Insert Content Controls:**
   - Use the XML Mapping pane to add Plain Text content controls for each dataset field.
   - Avoid Rich Text controls as they are not fully supported.
   - Manually enter column names in the first row.

4. **Save and Run Report:**
   - Save and close the Word document.
   - In Visual Studio Code, press Ctrl+F5 to compile and run the report in Business Central.
   - Search for and run the report in Business Central to view the generated layout.

5. **Add Images:**
   - Use Picture content controls to add images from the dataset.
   - Ensure images are in supported formats (.bmp, .jpeg, .png).

#### Tags
#reporting #dynamics365 #businesscentral #word #layouts #xmlmapping #dataset