# Hosting, Security, and PII

### Code executes in your cloud

When a user runs a stored procedure through Flank, the stored procedure executes on the database, and Flank merely returns the result. Same thing with an API call or an AWS Lambda. 

### Results are stored in your cloud

Flank stores the result of each run. The most common setup is to store the result in your cloud, either in AWS S3 or Azure Blob Storage.

### You control Flank's permissions

Flank has one entrypoint into your services, which you control. If you're using it with a database, you can create a database role specifically for Flank. If you're using it with AWS Lambda, you can create an AWS role specifically for Flank.

Basically, Flank needs two permissions:
1. An ability to "read" or gain awareness of stored procedures
2. An ability to execute whichever ones you want to expose

Additionally, if you're storing the run results in your cloud (see above), Flank needs permissions to read/write to a bucket that you create.

### You can host Flank yourself

Flank consists of 1) a single page app, 2) an API, 3) a database. If you want, you can host all three in your cloud.

### PII can be flagged and deleted

Flank stores the results of queries that users run (see above). These queries can contain PII. Depending on your retention policy, queries that contain PII can be flagged as such, and their results can be deleted on a rolling basis. For user-requested deletions, the results can be searched and deleted.