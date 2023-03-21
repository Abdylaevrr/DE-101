There you can find a couple of simple examples of analytical architecture solutions and example of an Excel dashboard. 

[Design Example 1](Module1/Analytical%20Solution%20Designs/Design%20Example%201.png) - an existing project on MS Azure cloud for one of Big Pharma companies. We have two main sources for our Data Warehouse - sales data that comes to SFTP server and OLTP Azure database (it stores drug sales data also) that is populated by a Desktop app. After that we use an Azure Data Factory (ADF) instance to move data from sources to our storage (another Azure database). ADF pipelines are triggered by both its own triggers and the Desktop app (manual management). As soon as the storage is updated, we start updating an OLAP cube. Further, business users can start analyse fresh data in their own tools (Excel, SQL editors or Power BI dashboards). 

[Design Example 2](Module1/Analytical%20Solution%20Designs/Design%20Example%202.png) - also was built for one of pharmacutical organization. 