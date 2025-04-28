## About the connector
Vectra provides automated threat detection, empowers threat hunting and exposes hidden attackers
<p>This document provides information about the vectra Connector, which facilitates automated interactions, with a vectra server using FortiSOAR&trade; playbooks. Add the vectra Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with vectra.</p>

### Version information

Connector Version: 4.0.0

Authored By: Fortinet

Certified: No
## Release Notes for version 4.0.0
Following enhancements have been made to the vectra Connector in version 4.0.0:
<ul>
<li>Get Accounts List</li>
<li>Get Detection By ID</li>
<li>Get Outcomes List</li>
<li>Get Assignments List</li>
<li>Get Groups List</li>
<li>Get Users List</li>
<li>Get Outcome By ID</li>
<li>Get Host By ID</li>
<li>Get Assignments By ID</li>
<li>Get Audit Log Events Associated with a User ID</li>
<li>Execute an API Request</li>
<li>Get Vectra Match Rules</li>
</ul>

<h2>Parameters are updated for following actions:</h2>

<ul>
<li>Get Threat Feeds</li>
</ul>

<h3>What's Removed</h3>

<ul>
<li>Get All Traffic Stats</li>
<li>Get Rules</li>
</ul>

## Installing the connector
<p>Use the <strong>Content Hub</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.</p><p>You can also use the <code>yum</code> command as a root user to install the connector:</p>
<pre>yum install cyops-connector-vectra</pre>

## Prerequisites to configuring the connector
- You must have the credentials of vectra server to which you will connect and perform automated operations.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the vectra server.

## Minimum Permissions Required
- Not applicable

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>vectra</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations</strong> tab enter the required configuration details:</p>
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Server URL</td><td>URL of the Vectra server to which you will connect and perform the automated operations.
</td>
</tr><tr><td>Client ID</td><td>Specify the client ID created to access vectra APIs.
</td>
</tr><tr><td>Client Secret</td><td>Specify the client secret created to access vectra APIs.
</td>
</tr><tr><td>Verify SSL</td><td>Specifies whether the SSL certificate for the server is to be verified or not. <br/>By default, this option is set to True.</td></tr>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function</th><th>Description</th><th>Annotation and Category</th></tr></thead><tbody><tr><td>Get Accounts List</td><td>Retrieves a list of accounts from Vectra based on the filters specified in the parameter.</td><td>get_accounts_list <br/>Investigation</td></tr>
<tr><td>Get Detections</td><td>Retrieves a list of detections from Vectra based on the filters specified in the parameter.</td><td>get_detections_list <br/>Investigation</td></tr>
<tr><td>Get Detection By ID</td><td>Retrieves a detections from Vectra based on the ID specified.</td><td>get_detection_by_id <br/>Investigation</td></tr>
<tr><td>Get Outcomes List</td><td>Retrieves a list of outcomes from Vectra.</td><td>get_outcomes_list <br/>Investigation</td></tr>
<tr><td>Get Hosts</td><td>Retrieves a list of hosts from Vectra based on the filters specified in the parameter.</td><td>get_hosts_list <br/>Investigation</td></tr>
<tr><td>Get Assignments List</td><td>Retrieves a list of assignments from Vectra based on the filters specified in the parameter.</td><td>get_assignments_list <br/>Investigation</td></tr>
<tr><td>Get Groups List</td><td>Retrieves a list of groups from Vectra based on the filters specified in the parameter.</td><td>get_groups_list <br/>Investigation</td></tr>
<tr><td>Get Users List</td><td>Retrieves a list of users from Vectra based on the filters specified in the parameter.</td><td>get_users_list <br/>Investigation</td></tr>
<tr><td>Get Outcome By ID</td><td>Retrieves a outcome from Vectra based on the ID specified.</td><td>get_assignment_outcome_by_id <br/>Investigation</td></tr>
<tr><td>Get Host By ID</td><td>Retrieves a host from Vectra based on the ID specified.</td><td>get_host_by_id <br/>Investigation</td></tr>
<tr><td>Get Assignments By ID</td><td>Retrieves a assignments from Vectra based on the ID specified.</td><td>get_assignments_by_id <br/>Investigation</td></tr>
<tr><td>Get Audit Log Events Associated with a User ID</td><td>Retrieves audit log events associated with a user ID</td><td>get_audit_log_events_associated_with_a_user_id <br/>Investigation</td></tr>
<tr><td>Execute an API Request</td><td>Sends an API request to any API endpoint based on specified HTTP method, endpoint, and other input parameters that you have specified, enabling flexible API interactions tailored to user needs.</td><td>send_custom_request <br/>Investigation</td></tr>
<tr><td>Get Threat Feeds</td><td>Retrieves a list of threat feeds from Vectra based on the filters specified in the parameter.</td><td>get_threat_feeds <br/>Investigation</td></tr>
<tr><td>Get Vectra Match Rules</td><td>Retrieves a list of rules from Vectra based on the filters specified in the parameter.</td><td>get_vectra_match_rules <br/>Investigation</td></tr>
</tbody></table>

### operation: Get Accounts List
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Minimum ID</td><td>Returns Accounts with an ID greater than or equal to the specified ID.
</td></tr><tr><td>Maximum ID</td><td>Returns Accounts with an ID less than or equal to the specified ID.
</td></tr><tr><td>Minimum Threat</td><td>Returns Accounts with a threat score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Threat</td><td>Returns Accounts with a threat score less than or equal to the specified score.
</td></tr><tr><td>Minimum Certainty</td><td>Returns Accounts with a certainty score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Certainty</td><td>Returns Accounts with a certainty score less than or equal to the specified score.
</td></tr><tr><td>State</td><td>Filters by state ('active', 'inactive'). Possible values are: active, inactive.
</td></tr><tr><td>Search Query</td><td>SearSearch query in Lucene query syntax.
</td></tr><tr><td>Search Query Only</td><td>Use specifically this search query. Compared to "search_query" where default arguments are appended.
</td></tr><tr><td>Minimum Privilege Level</td><td>Returns entries with a privilege level greater than or equal to the specified score.
</td></tr><tr><td>Maximum Privilege Level</td><td>Returns entries with a privilege level greater than or equal to the specified score.
</td></tr><tr><td>Privilege Category</td><td>Filters by the privilege category ("low", "medium", "high") provided.
</td></tr><tr><td>Tags</td><td>Filters by a tag or a comma-separated tags.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Detections
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Minimum ID</td><td>Returns detections with an ID greater than or equal to the specified ID.
</td></tr><tr><td>Maximum ID</td><td>Returns detections with an ID less than or equal to the specified ID.
</td></tr><tr><td>Minimum Threat</td><td>Returns detections with a threat score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Threat</td><td>Returns detections with a threat score less than or equal to the specified score.
</td></tr><tr><td>Minimum Certainty</td><td>Returns detections with a certainty score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Certainty</td><td>Returns detections with a certainty score less than or equal to the specified score.
</td></tr><tr><td>State</td><td>Filters by state ('active', 'inactive'). Possible values are: active, inactive.
</td></tr><tr><td>Search Query</td><td>Search query in Lucene query syntax.
</td></tr><tr><td>Search Query Only</td><td>Use specifically this search query. Compared to "search_query" where default arguments are appended.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Detection By ID
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Detection ID</td><td>Specify the detection ID to get the details.
</td></tr></tbody></table>
#### Output

 The output contains a non-dictionary value.
### operation: Get Outcomes List
#### Input parameters
None.
#### Output

 The output contains a non-dictionary value.
### operation: Get Hosts
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Minimum ID</td><td>Returns hosts with an ID greater than or equal to the specified ID.
</td></tr><tr><td>Maximum ID</td><td>Returns hosts with an ID less than or equal to the specified ID.
</td></tr><tr><td>Minimum Threat</td><td>Returns hosts with a threat score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Threat</td><td>Returns hosts with a threat score less than or equal to the specified score.
</td></tr><tr><td>Minimum Certainty</td><td>Returns hosts with a certainty score greater than or equal to the specified score.
</td></tr><tr><td>Maximum Certainty</td><td>Returns hosts with a certainty score less than or equal to the specified score.
</td></tr><tr><td>State</td><td>Filters by state ('active', 'inactive'). Possible values are: active, inactive.
</td></tr><tr><td>Search Query</td><td>Search query in Lucene query syntax.
</td></tr><tr><td>Search Query Only</td><td>Use specifically this search query. Compared to "search_query" where default arguments are appended.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Assignments List
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Account IDs</td><td>Filters by accounts IDs. You can specify multiple IDs as comma separated values.
</td></tr><tr><td>Assignee IDs</td><td>Filters by assignees IDs.You can specify multiple IDs as comma separated values.
</td></tr><tr><td>Host IDs</td><td>Filters by hosts IDs.You can specify multiple IDs as comma separated values.
</td></tr><tr><td>Outcome IDs</td><td>Filters by outcomes IDs.You can specify multiple IDs as comma separated values.
</td></tr><tr><td>Resolution State</td><td>Filters by resolution state.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Groups List
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Group Type</td><td>Filter by group type. Possible values are: account, host, ip, domain.
</td></tr><tr><td>Account Names</td><td>Filter by Account Names. Supports comma-separated values.
</td></tr><tr><td>Domains</td><td>Filter by Domains. Supports comma-separated values.
</td></tr><tr><td>Host IDs</td><td>Filter by Host IDs. Supports comma-separated values.
</td></tr><tr><td>Host Names</td><td>Filter by Host Names. Supports comma-separated values.
</td></tr><tr><td>Importance</td><td>Filter by group importance. Possible values are: high, medium, low, never_prioritize.
</td></tr><tr><td>IPs</td><td>Filter by IPs. Supports comma-separated values.
</td></tr><tr><td>Description</td><td>Filter by group description.
</td></tr><tr><td>Last Modified Timestamp</td><td>Return only the groups which have a last modification time equal to or after the given time.
</td></tr><tr><td>Last Modified By</td><td>Filters by the user id who made the most recent modification to the group.
</td></tr><tr><td>Group Name</td><td>Filters by group name.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Users List
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Username</td><td>Filters by user name.
</td></tr><tr><td>Role</td><td>Filters by user role.
</td></tr><tr><td>Type</td><td>Filters by type ('Local', 'SAML', etc). Possible values are: local, SAML etc.
</td></tr><tr><td>Last Login Datetime</td><td>Filters for Users that logged in since the given datetime.
</td></tr><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Outcome By ID
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Outcome ID</td><td>Specify the outcome ID to get the details.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Host By ID
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Host ID</td><td>Specify the host ID to get the details.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Assignments By ID
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Assignments ID</td><td>Specify the assignments ID to get the details.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Audit Log Events Associated with a User ID
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>User ID</td><td>Specify the user ID to get the details.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Execute an API Request
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>HTTP Method</td><td>Select an HTTP action for the request. You can select from the following options: DELETE GET PATCH POST PUT
</td></tr><tr><td>Endpoint</td><td>Specify the target API URL path for the request. For example, if the website is https://example.com and URL path is https://example.com/api/v2/incidents/search, the endpoint would be /api/v2/incidents/search.
</td></tr><tr><td>Query Parameters</td><td>(Optional) Specify any optional parameters to add to the URL and refine the request.
</td></tr><tr><td>Request Payload</td><td>(Optional) Specify data, as JSON, to be sent as the request payload (typically for POST or PUT requests).
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Threat Feeds
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Vectra Match Rules
#### Input parameters
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Query Parameter</td><td>Specify the parameters to filter the records. E.g. {'id': 123, 'statues' 'active'}.
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
## Included playbooks
The `Sample - vectra - 4.0.0` playbook collection comes bundled with the vectra connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR&trade; after importing the vectra connector.

- Execute an API Request
- Get Accounts List
- Get Assignments By ID
- Get Assignments List
- Get Audit Log Events Associated with a User ID
- Get Detection By ID
- Get Detections
- Get Groups List
- Get Host By ID
- Get Hosts
- Get Outcome By ID
- Get Outcomes List
- Get Threat Feeds
- Get Users List
- Get Vectra Match Rules

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection since the sample playbook collection gets deleted during connector upgrade and delete.