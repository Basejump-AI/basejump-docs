# Concepts

## User Definitions

### Administrator

An administrator is the account owner. The account owner can invite other team members and assign them as administrators or members. This same role-based access control (RBAC) is alos used in the API. The administrator can create client secret to provide others access to the API as well.

The administrator sidebar has additional items compared to a member. The following items are in addition to what a member has access to:
- Datasources
- Teams
- Company
- Subscription

![The sidebar](/images/sidebar.png)

Refer to the 'Sidebar Options' section for more information regarding each option:

[!ref](/sidebar-options/)

### Member

A member has less privileges than the administrator. The additional administrator privileges are listed above under 'Administrator.

![Invite company members](/images/company/invite_company_members.png)

### User

A User is either an administrator or member which has access to the Basejump AI application.

### Team

A team is a group of users who have been provisioned a certain level of access to various datasources.

![The team page](/images/team/team_page.png)

Datasources are assigned at the team level and not the individual user level. Results generated from datasources can be shared within teams.

### Datasources

A datasource is a connection to your data. This currently is focused on databases only, but will soon also include the ability to upload CSVs and other data source types.

## Data

### Data Object

A data object is a piece of retrieved data from your datasources. The data object can be 1 of 3 types:
- Metric
- Record
- Dataset

![The Data page in tabular view](/images/data/data_tabular_page.png)

### Metric

A metric is a data object that is 1 row by 1 column. When a metric is not being measured, it is known as a datapoint. In the Basejump UI, metrics are shown with a green gradient color and a box icon.

![A data tile of a metric example](/images/data/metric.png)

### Record

A record is a data object that is 1 row by many columns. In the Basejump UI, records are shown with an orange gradient and an ID icon.

### Dataset

A dataset is a data object that is many rows by many columns. In the Basejump UI, datasets are shown with a purple gradient and a table icon.