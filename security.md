# Security

Security is important to us so we have a few measures in place to ensure we are shipping secure software. There are many different aspects of security that we elaborate below to help explain our internal policies. We use multiple industry standard tools to ensure the security of our application.

## RBAC (Role-Based Access Control)
To help organizations provide access to only the data that should be seen by an individual, we use role-based access control. This is achieved through multiple methods at Basejump. One method is by using Teams. A Team is a group created by an administrator to limit data access. Each team may have access to different database connections. This is controlled by an administrator. Reports can only be shared within teams to ensure that requisite access has been provided to view the information. 

Additionally, when a database is added, the role associated with the username and password will be used to query the information. Therefore, the given database connection assigned to teams can only access the information based on that database role. 

Finally, when indexing the information to provide to our AI, we only index the metadata and not the table information itself. The AI also only will see the same tables that a user has permission to see. This ensures that the AI is unable to provide any information that a user is not permitted to access.

## AI
We only partner with AI providers who do not train on customer data. We only use the database metadata to inform the AI and never index the rows from your data sources.
API Access
Access to our API is provided using authentication and refresh tokens. All endpoints are secured using these tokens to ensure only authorized access. There are 4 levels of token access (in order of most to least access):
- API level
- Account Owner
- Admin
- Member

Using tokens ensures that API secrets are not used frequently. Refresh tokens are required to be refreshed every 90 days and authentication tokens need to be refreshed every 15 minutes. 

For more security information, please refer to our Basejump Security Policy: <put the Basejump security policy link here>
