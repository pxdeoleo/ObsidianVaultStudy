#### Main Features
- SaaS/On-Premise Controller
- User Interface and Reporting
- Correlated transaction views
- No code changes required
- Low overhead in production

Most [[AppDynamics]] agents work using one-way http/s communication from agent to the Application Intelligence Platform.

Some customers have tens of thousands agents.
#### Agents
These agents can be present in:
- End User Agents. Browser / Mobile / IoT. Begin the observability the moment the user has an interaction.
- [[ThousandEyes]]. Network / Device / Digital Experience. Monitor every network hop from frontend to backend application.
- Application Agent. Java / .NET / PHP / Node.js / C++ /  Python / Go / SAP. Deep visibility from code, being able to identify a single problematic line of code.
- Server Agent. OS / Cloud-Native ([[CloudWatch]], [[AppInsights]], [[X-ray]]). Check hardware health i.e. disk I/O, memory usage.
- Database. SQL/ noSQL / Cloud (Aurora). This one doesn't use HTTP/S communication, but a remote JDBC. Optimize queries and identify areas of improvement.

When the observability data reaches the platform, the [[Cognition Engine]] uses the data to alert the necessary team. The [[Application Intelligence Platform]] (or Controller) can be deployed in a Cloud or OnPremise environment.