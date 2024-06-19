## Controller class
It's the execution class.
Holds info about:
- Dialog
- Execution mode
- Progress bar
- etc

```C#
internal final class MySysOperationController extends SysOperationServiceController
{
    protected void new()
    {
        super(classStr(mySysOperationService), methodStr(MySysOperationService, process), SysOperationExecutionMode::Synchronous);
    }

    public ClassDescription defaultCaption()
    {
        return "My process job";
    }

    public static MySysOperationController construct(SysOperationExecutionMode _executionMode = SysOperationExecutionMode::Synchronous)
    {
        MySysOperationController controller;
        controller = new MySysOperationController();
        controller.parmExecutionMode(_executionMode);

        return controller;
    }

    public static void main(Args _args)
    {
        MySysOperationController controller;

        controller = MySysOperationController::construct();
        controller.parmArgs(_args);
        controller.startOperation();
    }
}
```