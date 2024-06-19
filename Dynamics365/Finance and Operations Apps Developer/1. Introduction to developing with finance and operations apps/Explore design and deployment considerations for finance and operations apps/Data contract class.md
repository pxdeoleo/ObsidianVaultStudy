## Data contract class
Indicates the attributes needed for the job. The attributes automatically provide a dialog-based UI.

```C#
[DataContractAttribute]
internal final class MySysOperationContract
{
    private ItemId      itemId;

    [DataMember, SysOperationLabel(literalStr("Item Id")), SysOperationHelpText(literalStr("Item Id help")), SysOperationDisplayOrder('1')]
    public ItemId parmItemId(ItemId _itemId = itemId)
    {
        itemId = _itemId;

        return itemId;
    }
}
```
