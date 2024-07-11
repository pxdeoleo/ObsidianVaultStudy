>[!summary]
>Customize [[Business Central]] fields in Teams using field groups or events. The Brick field group is recommended but not required, and the order of fallback is Brick, Dropdown, or primary key fields. Events offer additional customization options.

#### Customizing Fields for Teams
- Use Brick, Dropdown, or primary key fields for displaying cards in Teams.
- Brick field group is recommended for a consistent experience.
- Templates determine field order based on presence of media fields.

>[!info] Field Groups
- **Brick Field Group:** Specifies which fields display on a Teams card.
- **Dropdown Field Group:** Used if Brick field group is absent.
- **Primary Key Fields:** Used if both Brick and Dropdown field groups are absent.

>[!example] Brick Field Group Code Example
```AL
fieldgroups
{
    fieldgroup(Brick; Number, Description, Image)
    {
    }
}
```

#### Templates for Field Order
- **With Media:**
  1. Second field in Brick field group (in large font).
  2. Page caption property value.
  3. Media thumbnail.
  4. Remaining Brick fields in order.
- **Without Media:**
  1. Page caption property value.
  2. Second field in Brick field group.
  3. Remaining Brick fields in order.

#### Events for Customization
- **OnBeforeGetPageSummary:** Override all data for a card, specify custom key-value pairs.
- **OnAfterGetSummaryFields:** Add or remove fields from the same table, ideal for extended tables.
- **OnAfterGetPageSummary:** Modify, add, or remove fields already selected for the card.

>[!info] Using OnBeforeGetPageSummary Event
- Provides full control over card fields and data.
- Use JSON array to specify fields.
```AL
[EventSubscriber(ObjectType::Codeunit, Codeunit::"Page Summary Provider", 'OnBeforeGetPageSummary', '', false, false)]
local procedure OnBeforeGetPageSummary(PageId: Integer; RecId: RecordId; FieldsJsonArray: JsonArray; var Handled: Boolean)
var
    Vendor: Record Vendor;
begin
    if PageId <> Page::"Vendor Card" then
        exit;

    if not Vendor.Get(RecId) then
        exit;

    AddField(FieldsJsonArray, 'Name', Vendor.Name, 'Text');
    AddField(FieldsJsonArray, 'Note', 'Added by extension', 'Text');
    AddField(FieldsJsonArray, 'Address', Vendor.Address, 'Text');
    AddField(FieldsJsonArray, 'Phone No.', Vendor."Phone No.", 'Text');

    Handled := true;
end;

local procedure AddField(var FieldsJsonArray: JsonArray; Caption: Text; FieldValue: Text; FieldType: Text)
var
    FieldsJsonObject: JsonObject;
begin
    FieldsJsonObject.Add('caption', Caption);
    FieldsJsonObject.Add('fieldValue', FieldValue);
    FieldsJsonObject.Add('fieldType', FieldType);
    FieldsJsonArray.Add(FieldsJsonObject);
end;
```

#### Using OnAfterGetSummaryFields Event
- Add or remove fields from the selected list.
- Ensure fields are in the correct order.
```AL
[EventSubscriber(ObjectType::Codeunit, Codeunit::"Page Summary Provider", 'OnAfterGetSummaryFields', '', false, false)]
local procedure OnAfterGetSummaryFields(PageId: Integer; RecId: RecordId; var FieldList: List of [Integer])
var
    Vendor: Record Vendor;
begin
    if PageId <> Page::"Vendor Card" then
        exit;

    FieldList.Remove(Vendor.FieldNo("Balance Due (LCY)"));
    FieldList.Remove(Vendor.FieldNo("Balance (LCY)"));
    FieldList.Add(Vendor.FieldNo("Phone No."));
    FieldList.Add(Vendor.FieldNo("Vendor Role Name"));
end;
```

#### Using OnAfterGetPageSummary Event
- Modify existing field values or add new fields.
```AL
[EventSubscriber(ObjectType::Codeunit, Codeunit::"Page Summary Provider", 'OnAfterGetPageSummary', '', false, false)]
local procedure OnAfterGetPageSummary(PageId: Integer; RecId: RecordId; var FieldsJsonArray: JsonArray)
var
    FieldJsonToken: JsonToken;
    CaptionToken: JsonToken;
    fieldNo: Integer;
begin
    if PageId <> Page::"Vendor Card" then
        exit;

    for fieldNo := 0 to FieldsJsonArray.Count() - 1 do begin
        FieldsJsonArray.Get(fieldNo, FieldJsonToken);
        FieldJsonToken.AsObject().Get('caption', CaptionToken);
        if CaptionToken.AsValue().AsText() = 'Contact' then begin
            FieldJsonToken.AsObject().Replace('caption', 'Note');
            FieldJsonToken.AsObject().Replace('fieldValue', 'Added by extension');
            FieldsJsonArray.Set(fieldNo, FieldJsonToken);
            exit;
        end;
    end;
end;
```