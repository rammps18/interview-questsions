How did you handle and optimize timeout issues in Azure DevOps pipelines?

Here is my explanation:

1.Identified the timeout point:
 Usually during npm install or long-running tests. I checked pipeline logs to find the bottleneck.
2.Increased timeoutInMinutes in YAML
3.Optimized npm installs:
 Used flags like --prefer-offline and --no-audit to reduce network delays.
4.Added caching for node_modules:
 Helped avoid redundant downloads and speed up builds.
5.Switched to self-hosted agents:
 Faster builds and no dependency on Microsoft-hosted agent queues.
6.Split the pipeline into smaller jobs:
 Each job handled a specific task (build, test, deploy) — easier to debug and faster to execute.
7.Scheduled heavy builds during off-peak hours:
 Reduced agent queue times and throttling risks.
