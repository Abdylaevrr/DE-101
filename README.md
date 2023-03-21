There you can find a couple of simple examples of analytical architecture solutions and an example of an Excel dashboard.

[Design Example 1](Module1/Analytical%20Solution%20Designs/Design%20Example%201.png) is an existing project on MS Azure cloud for one of Big Pharma's companies. We have two main sources for our Data Warehouse - sales data that comes to an SFTP server and OLTP Azure database (it stores drug sales data also) that is populated by a Desktop app. After that, we use an Azure Data Factory (ADF) instance to move data from sources to our storage (another Azure database). ADF pipelines are triggered by both its own triggers and the Desktop app (the manual management). As soon as the storage is updated, we start updating an OLAP cube. Further, business users can start to analyze fresh data with their own tools (Excel reports, SQL editors, or Power BI dashboards).

[Design Example 2](Module1/Analytical%20Solution%20Designs/Design%20Example%202.png) has been also built for one of pharmacutical organization. There we have at least four sources:

1. Text files from FTP server
2. Web-pages - we use scrapping to catch new data from web-pages directly
3. OpenStreetMaps (OSM) - we want to upload information about OSM polygons to use them on our Qlik maps
4. Different ad-hoc csv files (usually some static dictionaries)