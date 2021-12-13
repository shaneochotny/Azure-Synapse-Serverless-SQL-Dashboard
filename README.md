# Azure Synapse Serverless SQL Dashboard

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Dashboard-Overview.gif)

# Description

A Workbook for Log Analytics that provides a dashboard view of Azure Synapse Serverless SQL usage including estimated costs, data processed, query activity, and user activity.

# How to Deploy

### Enable Azure Synapse Analytics Diagnostic Logging
This workbook requires the Synapse Analytics Workspace Diagnostic Settings be enabled and sending log data to Log Analytics. You need atleast <b>BuiltinSqlReqsEnded</b> enabled, but enabling the other categories is fine too.

1. In the Synapse workspace resource, select <b>Diagnostic settings</b> from the navigation menu and then select <b>Add diagnostic setting</b>.

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Synapse-Diagnostics-Step-1.png)

2. Specifiy the diagnostic setting name, such as "<b>Diagnostics</b>". Next, select <b>BuiltinSqlReqsEnded</b>. Enabling the other categories is fine too. Finally, check <b>Send to Log Analytics workspace</b> and specify the <b>Subscription</b> and <b>Log Analytics workspace</b> you want Synapse to log to.

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Synapse-Diagnostics-Step-2.png)


### Create the Workbook
The workbook can be manually added to your Log Analytics Workspace by following the below steps.

1. In your Log Analytics workspace, select <b>Workbooks</b> from the navigation menu and then select <b>New</b>.

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Workbook-Step-1.png)

2. Click the <b>Advanced Editor</b> button from the top menu.

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Workbook-Step-2.png)

3. Select and delete all the default JSON. Next, copy and paste the JSON contents from the <b>Synapse-Serverless-SQL-Dashboard.json</b> file into the editor and click <b>Apply</b>.

![alt tag](https://raw.githubusercontent.com/shaneochotny/Azure-Synapse-Serverless-SQL-Dashboard\/main/images/Workbook-Step-3.png)