>[!summary]
Rich text editing in [[Business Central]] enhances user experience by enabling the creation and editing of multimedia content. This feature is ideal for unstructured information, allowing for text, tables, links, and images.

#### Definitions
- **Rich Text Editor**: A tool that provides a multiline textbox with a rich toolbar for multimedia content creation.

>[!info] Capabilities
- Suitable for multimedia content like social media posts, emails, annotations, and file contents.
- Allows for adding and formatting text, tables, images, and hyperlinks.

>[!info] Features
- **Multiline textbox** with rich formatting toolbar.
- **Keyboard shortcuts** for various text formatting options.
- Embeds media directly in HTML content.
- Persist content as HTML in a Blob field in the database.
  
#### Usage
- **Blob, BigText, and Text data types**: The rich text control can be applied without size limits.
- **Control placement**: Must be placed alone in a group (e.g., FastTab) on a page.
- **Email Editor**: A common use case requiring significant screen space.

#### Code Example
**Creating a Rich Text Editor backed by a Blob field**:
```al
table 50100 MyTable
{
    fields
    {
        field(1; MyIntegerField; Integer) { }
        field(2; RichTextBlob; Blob) { Description = 'Contains a rich text value'; }
    }

    procedure GetRichText(): Text
    var
        InStream: Instream;
        TextValue: Text;
    begin
        Rec.CalcFields(Rec.RichTextBlob);
        Rec.RichTextBlob.CreateInStream(InStream);
        InStream.ReadText(TextValue);

        exit(TextValue);
    end;

    procedure SaveRichText(RichText: Text)
    var
        OutStream: OutStream;
    begin
        Rec.RichTextBlob.CreateOutStream(OutStream);
        OutStream.WriteText(RichText);
        Rec.Modify();
    end;
}

page 50100 MyPage
{
    PageType = Card;
    SourceTable = MyTable;

    layout
    {
        area(Content)
        {
            group(FastTabGroup)
            {
                field("Rich Text Editor"; RichText)
                {
                    Caption = 'My Rich Text Editor.';
                    ExtendedDataType = RichContent;
                    MultiLine = true;

                    trigger OnValidate()
                    begin
                        Rec.SaveRichText(RichText);
                    end;
                }
            }
        }
    }
    
    trigger OnAfterGetCurrRecord()
    begin
        RichText := Rec.GetRichText();
    end;

    var
        RichText: Text;
}
```

#### Tips
- **Toolbar limitations**: Customization of the toolbar is not supported.
- **UI customization**: Limited options for UI customization through personalization.
- **Field constraints**: Cannot set RichContent value directly on a table field; compiler error will occur.
- **Placement constraints**: Must be on a root-level group (e.g., FastTab) and be the only control in that group.

#### Tags
#BusinessCentral #RichTextEditor #MultimediaContent #ALCode #BlobField #UserExperience