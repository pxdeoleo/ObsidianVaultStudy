## Service class
It's actual code that's processed.
```C#
internal final class MySysOperationService extends SysOperationServiceBase
{
    public void process(MySysOperationContract _contract)
    {
        // do something

        ItemId itemId = _contract.parmItemId();

        Info(strFmt("%1", itemId));
    }
}
```