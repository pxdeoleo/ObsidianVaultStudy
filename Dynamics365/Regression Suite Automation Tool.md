>[!summary]
>The Regression Suite Automation Tool (RSAT) enhances the efficiency of User Acceptance Testing (UAT) for finance and operations apps by automating test creation and execution through integration with [[Task Recorder]] and Azure DevOps.

#### Definitions
- RSAT (Regression Suite Automation Tool): A tool designed to automate the process of recording, configuring, and executing user acceptance tests for [[Dynamics 365 Applications]].

>[!info] Integration with Azure DevOps

RSAT integrates seamlessly with Microsoft Azure DevOps, facilitating test execution, [[Reporting]], and investigation, with test parameters managed through Microsoft Excel for flexibility.

>[!bug] Limitations in Test Scope

RSAT is optimized for business cycle and scenario testing and is not recommended for unit or integration testing, where other frameworks like SysTest or DIXF should be used.

>[!info] RSAT Workflow

The end-to-end testing flow with RSAT involves authoring tests using [[Task Recorder]], configuring tests in Azure DevOps, and executing them through RSAT, supported by Dynamics [[Lifecycle Services]] (LCS) for broader test management.

>[!tip] Effective Use of [[Task Recorder]]

Utilize [[Task Recorder]] to create detailed recordings of business processes, which can then be converted into automated tests without the need for manual coding.

>[!attention] Test Classification and Scope

RSAT is ideally used for testing larger business processes or scenarios that reflect end-user interactions with the application at the end of the development lifecycle.

>[!example] Setting Up and Running Tests with RSAT

1. Record business processes using [[Task Recorder]].
2. Save recordings as developer files and attach them to test cases in Azure DevOps.
3. Configure RSAT to manage and execute these tests, ensuring alignment with business requirements.
4. Review test outcomes and adjust as necessary to refine the testing process.

>[!info] RSAT [[User Interface]] and Navigation

The RSAT [[User Interface]] is designed for ease of use, featuring a modern layout with quick links and easy navigation to essential components like test plans and settings.

#### Additional Tools and Recommendations
- **For Unit Testing**: Use the SysTest framework along with the Acceptance Test Library (ATL) for creating consistent test data and readable test code.
- **For Integration Testing**: Employ the Data Management Framework (DIXF) instead of RSAT to ensure robust data integration testing.

>[!info] Leveraging RSAT for Effective UAT

Adopting RSAT for user acceptance testing significantly reduces time and resource expenditure, allowing teams to focus on delivering high-quality updates and customizations in finance and operations apps.