Operate
=================

## Platform application logging
All application and microservices that follow the ECOMP Platform application logging guidelines have the following common types, location, and syntax. Each message includes a unique ID to capture the flow of requests across OpenECOMP components and enable the tracing, understanding, and troubleshooting of performance across the ECOMP platform.
The ONAP Application Logging Guidelines document is the official source for logging details.

### Log types
* Audit: Captures the high-level activities carried out by OpenECOMP components as a result of incoming requests, including API requests,job executions, and messages received. Required.
* Metric: Captures the detailed activities required to carry our the activities recorded by the Audit logs, specifically outbound messages and activities. Required.
* Error: Captures error conditions for the application. There are four error severity levels (info, warn, error, fatal). Required.
* Debug: Captures data required to correct abnormal conditions. Optional.

### Log files
Each type of log is stored in a separate file. A full directory path is not specified, but all log directories have the following structure:
<log-directory>/<ecomp-component>/<ecomp-subcomponent>/[audit.log | metric.log | error.log | debug.log]

### Logging frameworks
Java components use EELF (Event and Error Logging Framework).

### Log fields
See the ONAP Application Logging Guidelines for descriptions of all fields for each log type.

## Managing Policies
This section describes how to manage generic policy using the Policy application. For information on creating policy and pushing it to PDPs, see Policy Design.

### Remove policies from a PDP Group
Policy is activated when pushed to a Policy Distribution Point (PDP) and retrieved from the PDP by a policy client. To remove an active policy in the Policy application, remove it from any PDP group to which it was pushed.
1. Sign in to the Policy application as a Policy Editor.
2. Click Push.
3. In the PDP Groups pane, locate the row of the PDP group containing the policy to remove and click .
   The Remove PDP Group Policies box displays.
4. Select a policy by clicking the check mark in its row. Repeat as necessary to select multiple policies.
5. Click Remove to remove selected policies from the PDP group.

A success message displays after policies are removed from the PDP group.

### Disable an active policy
To disable an active policy, use the same process for removing policies from a PDP group. When a policy is removed from the PDP group(s) to which it was pushed, policy clients can no longer use the policy. See Remove policies from a PDP Group above.

