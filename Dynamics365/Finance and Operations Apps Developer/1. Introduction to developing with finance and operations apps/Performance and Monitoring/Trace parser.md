>[!summary]
>Trace parser is a performance tracking tool for Finance and Operations apps. It records a set of steps, and helps identify performance issues, long-running X++ methods, or bottlenecks hidden in heavy requests.

#### Definitions
- Performance analyzer for finance and operations app deployment.

>[!info] Traces

Traces record events of interaction between components of the systems. Kind of like logs.

>[!bug] Avoid

Before capturing a trace, avoid having metadata and other tasks included in it. For this, you must ensure you have completed the list of tasks you want to analyze; **no more, no less**.
>[!info] Location

Trace parser is located in the **PerfSDK** folder on the development environment deployments.

>[!tip] Multiple small traces

If the sequence of events takes more than a few minutes, **it is better to use multiple, smaller traces**.

>[!attention] System tracing user role

System tracing user role must be added to the user through **System administration > Users > Users**

>[!example] Start trace

1. In the navigation bar at the top-right of the screen, select the question mark icon
2. In the drop-down menu, select **Trace**
3. In the new screen, name the trace to be captured, and select **Start trace**
4. Perform all the actions to capture
5. Select **Stop trace**
6.  
	a. Select **Download trace** for it to be analyzed in the desktop version of Trace parser. 
	b. Select **Upload trace** to store it in the cloud, for downloading it at a different time. **It will be deleted after seven days**.

>[!info] Diagnose issues

Trace parser can help identify performance issues, such as long-running X++ methods, time-consuming SQL queries, or client server calls.
>[!info] Environment availability

 Trace parser is only available on [[DevTest topology]] deployed environments, it is not available in [[Demo topology]] environments.
