> [!summary] 
> Configure and run BCPT suites to simulate performance tests with specific parameters, concurrent sessions, and durations.

> [!info] Configuration Steps

1. **Specify Tests and Parameters**:
    
    - Select the tests to run and their parameters.
    - Define the number of concurrent sessions for each test.
    - Set the duration of the scenario.
2. **Run Modes**:
    
    - **Single Run Mode**: For quick tests during development. Runs all tests once, skips user delays, helps identify early regressions.
    - **Multiple Sessions**: Up to 500 concurrent sessions. Allows monitoring SQL statements and defining baselines.

> [!info] Execution

- **Foreground vs. Background**:
    - Foreground tests run sequentially if multiple are selected.
    - Background tests run in parallel. Use Visual Studio Code extension or PowerShell for multiple foreground tests.

> [!tip] Configuration Details

1. **BCPT Suites**:
    
    - Search for and create new BCPT Suite.
    - Provide identifier, description, and tag for tracking results.
2. **Define Timing**:
    
    - Use "1 Work Day Corresponds to" and "Duration (minutes)" fields.
    - Specify default user delays to simulate pauses between actions.
3. **Suite Lines**:
    
    - Enter test parameters without spaces.
    - Define concurrent sessions, user delays, delay between interactions, and delay type (Fixed or Random).

> [!example] Running Tests

1. **From Business Central**:
    
    - Direct execution within the application.
2. **Visual Studio Code Extension**:
    
    - Run BCPT: Run BCPT (PowerShell) command.
    - Select environment type and specific environment.
    - Enter BCPT suite code to run.
3. **PowerShell Scripts**:
    
    - Run tests via scripts for automation and flexibility.

> [!info] Analysis

- **Results Fields**:
    
    - **No. of Iterations**: Times the test ran.
    - **Total Duration (ms)**: Time taken for one iteration.
    - **Average Duration**: Summed time over multiple runs since baseline.
    - **No. of SQL Statements**: SQL statements generated per run.
    - **Avg. No. of SQL Statements**: Averaged over multiple runs.
- **Baseline and Delta**:
    
    - Compare current run results with baseline to identify changes.
    - **Change in No. of SQL Statements (%)**: Percent difference.
    - **Changes in Duration (%)**: Time difference between runs.

> [!tip] Log Entries

- **Filters**:
    - Use tags and filters to isolate specific runs and errors.
    - Export to Excel for advanced analysis with pivot tables.

> [!info] Telemetry

- **Enable Telemetry**:
    - Track performance toolkit events for deeper analysis using Power BI or KQL.

> [!bug] Additional Tips

- **Concurrency Limits**:
    
    - Client foreground: One session at a time.
    - Environment limits: Default is 10 sessions for background tasks.
- **Tags**:
    
    - Use tags to differentiate between various runs and scenarios.