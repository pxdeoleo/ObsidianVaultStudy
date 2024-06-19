>[!summary]
>Performance SDK is used for load testing in Finance and Operations apps, simulating real-life load conditions to ensure system stability under normal user activities.

#### Definitions
- Load testing: Performance testing under simulated real-life operations for single or multiple users.

>[!info] Load Testing Basics

Load testing involves simulating normal and peak conditions to evaluate how systems perform under various types of loads, ensuring that business processes function correctly without disruption.

>[!bug] Setup Accuracy

Before running a performance test, ensure the development environment is correctly set up with all necessary configurations and files, as inaccurate setup can lead to misleading test results.

>[!info] Performance SDK Location

The Performance SDK and related tools are primarily managed within the Visual Studio environment, requiring specific configurations and file placements.

>[!tip] Test Isolation

For accurate results, perform single-user tests before multi-user scenarios to isolate performance issues more effectively.

>[!attention] User Roles for Testing

Ensure that appropriate user roles and permissions are configured in both development and sandbox environments for test execution.

>[!example] Start Load Test

1. In Visual Studio, open the Test Explorer.
2. Locate your loaded test case.
3. Run the test and observe the performance metrics.
4. Adjust configurations if necessary and rerun the test for accurate benchmarks.
5. Document the test results for future reference and troubleshooting.

>[!info] Test Configuration

Ensure that your development and sandbox environments are aligned in terms of application and platform updates to avoid inconsistencies during testing.

>[!info] Environment Preparation

Prepare both development and sandbox environments by installing necessary certificates and configuring users to replicate real-life operational conditions.