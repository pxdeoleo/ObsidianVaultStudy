> [!summary] 
> The in-client performance profiler helps consultants and customer admins perform initial performance investigations without needing pro developers. It identifies performance issues and supports case filing to app owners. The profiler page can be opened from the Help & Support page and captures user flow performance data, including time spent per extension, top method calls, and other metrics.

#### Definitions

- **Performance profiler**: A tool for capturing and analyzing performance data within the Dynamics 365 Business Central application.

> [!info] Usage

The performance profiler captures data only for the current session and user who starts it. It can be opened alongside the user experience being profiled to ensure captures are concise.

> [!info] Insights Provided

1. **Active Apps Chart**: Shows potential speed improvements by removing specific apps.
2. **Time Spent Chart**: Displays time taken by each app during a process, available when "Show technical information" is toggled on.

> [!example] Launching Performance Profiler

1. In Business Central, select the **?** in the top menu.
2. Select **Help & Support**.
3. Click **Analyze performance** at the bottom of the Help & Support page.
4. The Performance Profiler window opens separately.
5. Click **Start** in the Performance Profiler window.
6. Perform the task to analyze in Business Central.
7. Click **Stop** in the Performance Profiler window to end the session.
8. View profiling results, including time spent per extension and other metrics.
9. Toggle **Show technical information** to view detailed performance data.

> [!tip] Separate Window

Open the Performance Profiler page in a separate browser window for easier management and navigation.

> [!info] Technical Details

- **Time Spent by Application Object**: Details on objects involved in the process, including time active and sampling frequency.
- **Call Tree**: Provides Self Time (time spent in the method only) and Total Time (Self Time plus calls out).

> [!info] Sharing Captures

- Download and share the profiling results file via OneDrive for further analysis by technical support or pro developers.

> [!note] Advanced Analysis

The Performance Profiler is a simplified version of the AL Profiler in Visual Studio Code. For detailed investigations, use the performance profiling editor view in Visual Studio Code to analyze top-down and bottom-up call stack views.