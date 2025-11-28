# Snowflake-pro
What are the three key layers of Snowflake’s architecture? Storage Layer, processing layer and cloud services layer
What is the name of the new web interface for Snowflake? snowsight
How can you change your password or security role in Snowsight? by using the profile section
What are the two types of warehouses available in Snowflake? standard and snowpark optimized
Which of the following terms are synonyms for a virtual warehouse in Snowflake? warehouse, compute resource, compute cluster
Which of the following data types are not supported by Snowflake? bit (date,time,boolean supported)
What is the standard data retention period for Time Travel in Snowflake? In days. 1
What is the name of the function that returns the ID of a specified query in the current session? LAST_QUERY_ID()
What is the default argument for the function LAST_QUERY_ID? -1
What is the effect of using the OVERWRITE option on INSERT? It deletes the existing records in the target table before inserting the new values 
What are the three usage types that Snowflake separates the cost of accomplishing any task into? data transfer, storage and Compute
What are the three types of compute resources that consume credits within Snowflake? Virtual warehouse, serverless, cloud services 
What is the name of the command that can load data from files into a table? Copy into
What is the individual file size limit for Snowsight? (In MBs) 250
What type of stage provides the greatest degree of flexibility for data loading? Named Stage
For data loads where we have multiple users and multiple tables involved, what is the recommended stage? Named Stage
What type of stage cannot be altered or dropped? User Stage, Table Stage
What type of stage is referenced using @~? Use Stage
What type of stage is referenced using @%? Table Stage
What is the command used to unload data from a Snowflake table into files? COPY INTO
What is the purpose of using the to_binary function in Snowflake? To convert string value to binary
What is the default value for the COMPRESSION file format option for CSV files? GZIP
What is the name of the file format option that specifies whether to skip any blank lines in the data files? SKIP_BLANK_LINES
What is the purpose of the NULL_IF file format option? To specify one or more  string value that should convert to null
What is the name of the authentication method that requires a public/private key pair with RSA encryption when calling the Snowpipe REST endpoints? JWT, JSON Web token
Load History stored for Bulk load metadata and Snowpipe metadata respectively? (In Days) 64 and 14
What is the purpose of creating a stream on a table or a view? To track the changes to the source object over time
What is the name of the hidden column that indicates the DML operation recorded by a stream?METADATA$ACTION
What is the condition that makes a stream stale and inaccessible? stream object is outside the retension period
What is the name of the SQL command that manually triggers a single run of a scheduled task? EXECUTE TASK
What does the USER_TASK_MANAGED_INITIAL_WAREHOUSE_SIZE parameter do in Snowflake? Specifies the size of the compute resources to provision for the first run of the task, before a task history is available for snowflake to determine the ideal size
Which of the following is a valid way to specify the record delimiter for CSV files to be loaded? RECORD_DELIMITER='<character>' OR NONE
What is the keyword that can be used instead of query_id to validate the last load executed during the current session? _LAST
What are the 2 types of UDFs in snowflake? Scalar and Tabular
How can you call a UDF in Snowflake? with SELECT statement
What is the name of the column that indicates the staleness status of a stream? STALE_AFTER
Which of the following is a valid way to specify the compression algorithm for the data files to be loaded?COMPRESSION = AUTO | GZIP | BZ2 | BROTLI | ZSTD | DEFLATE | RAW_DEFLATE | NONE
Which of the following is a valid way to specify the record delimiter for CSV files to be loaded? RECORD_DELIMITER = ‘<character>’ or NONE
What is the name of the function that validates the files loaded in a past execution of the COPY INTO <table> command? VALIDATE
What is the keyword that can be used instead of query_id to validate the last load executed during the current session?_LAST
Which of the following is a valid way to specify the error handling for the load operation? ON_ERROR = CONTINUE | SKIP_FILE | SKIP_FILE_num | ‘SKIP_FILE_num%’ | ABORT_STATEMENT
What is the difference between a UDF and a stored procedure in Snowflake? A UDF is a function that can be called from SQL, while a stored procedure is a script that can be executed with the CALL statement
What is the name of the parameter that specifies the number of days for which Snowflake retains historical data for Time Travel actions on an object? dat_retention_time_in_days
What are some best practices to avoid data unavailability errors when cloning tables with zero data retention time?Setting the DATA_RETENTION_TIME_IN_DAYS=1 before cloning and refrain from executing DML transactions on the source table
What can cause a data unavailability error when cloning a table with zero data retention time?Executing DML transactions on the source table during cloning
What is the name of the function that can be used to query semi-structured data in Snowflake?FLATTEN
What is the name of the property of semi-structured data that allows it to be loaded into relational tables without requiring a schema in advance in Snowflake? Schema-on-read
Which of these Snowflake format supported by Snowflake? json,avro,xml,parquet,ORC
What is the name of the function that generates a scoped Snowflake-hosted URL to a staged file?BUILD_SCOPED_FILE_URL
What is the name of the feature that stores a catalog of staged files in cloud storage? Directory tables
What is the name of the parameter that specifies the length of time for a pre-signed URL to be valid? expiration_time
What is the name of the function that returns the URL for an external or internal named stage using the stage name as the input?GET_STAGE_LOCATION
What is the name of the function that extracts the path of a staged file relative to its location in the stage using the stage name and absolute file path in cloud storage as inputs?GET_RELATIVE_PATH
What is the name of the function that generates a Snowflake-hosted file URL to a staged file using the stage name and relative file path as inputs?BUILD_STAGE_FILE_URL
What is the difference between STORAGE_ALLOWED_LOCATIONS and STORAGE_BLOCKED_LOCATIONS for a storage integration in Snowflake?STORAGE_ALLOWED_LOCATIONS defines which storage locations can be accessed by the stages utilizing the integration, while STORAGE_BLOCKED_LOCATIONS specifies which locations are off-limits for those same stages. 
What is the syntax for creating or replacing a storage integration in Snowflake? CREATE OR REPLACE STORAGE INTEGRATION sample_int
TYPE = EXTERNAL_STAGE
What is the name of the keyword generates a unique value in SEQUENCE?NEXTVAL
What is the sampling method that is not supported for fixed-size sampling?SYSTEM | BLOCK
What is the maximum number of rows that can be requested for fixed-size sampling?1000000
What is the effect of specifying a seed value for sampling? Specifying a seed value for sampling makes the process deterministic because it ensures that the same sample can be generated consistently across multiple runs.
What algorithm does Snowflake use to estimate the approximate number of distinct values in a data set?HLL(HyperLoglog)
What is the name of the partitioning technique used by Snowflake Data Platform?Micro-partitioning
What is the range of uncompressed data size for each micro-partition in Snowflake? 50-500MB
What is the term used to describe the average depth of overlapping micro-partitions for specified columns in a table? clustering depth
What is the benefit of storing columns independently within micro-partitions?efficient scanning, compression and pruning
What is the system function that can be used to view the clustering metadata for a table?SYSTEM$CLUSTERING_INFORMATION
How long (Hours) does Snowflake persist query results in the query result cache? 24
What is the purpose of the metadata cache in Snowflake?To store metadata about tables and columns
What is the name of the tool that provides execution details for a query in Snowflake?Query Profile
What information can you find in the Node List section of the Query Profile page? The execution time for each node
What information can you find in the Operator Tree section of the Query Profile page?the amount of data scanned by each operator
Which of the following functions can be used to estimate the cost of adding search optimization to a table? SYSTEM$ESTIMATE_SEARCH_OPTIMIZATION_COSTS
Which of the following statements is true about search optimization and Time Travel?search optimization specifically targets active data, meaning it does not enhance the performance of queries that leverage Time Travel, which deals with historical data.
How can you identify the queries that might benefit from the query acceleration service?By using the QUERY_ACCELERATION_ELIGIBLE view or the SYSTEM$ESTIMATE_QUERY_ACCELERATION function
What is the main purpose of the query acceleration service?designed specifically to handle outlier queries by distributing their processing workloads to shared compute resources, thus improving overall system efficiency and performance.
What is the name of the schema that provides cost information for the account?ACCOUNT_USAGE
What are the two access control models that Snowflake combines? Discretionary Access Control and Role-based Access Control
What is a securable object in Snowflake? An entity that can be accessed by other entitie
What is the difference between a primary role and a secondary role? primary role in Snowflake indeed determines the ownership of objects created during a session, defining who has control over those objects, while a secondary role only provides additional privileges without ownership implications
What is the name of the schema-level object that determines whether a given row in a table or view can be viewed from certain types of statements? Row Access Policy
What is the name of the feature that uses masking policies to selectively mask plain-text data in table and view columns at query time? dynamic data masking
What is the name of the service that powers MFA in Snowflake? Duo
What is the name of the parameter that enables MFA token caching for an account?ALLOW_CLIENT_MFA_CACHING
What is the role of Snowflake in a federated environment?SP
Which of the following vendors provide native Snowflake support for federated authentication and SSO?Okta and AD FS
What is the name of the shared database that provides historical usage data for all accounts in an organization?SNOWFLAKE
What is the purpose of the CURRENT_REGION context function?To retrieve the region in which your account is located
What type of IP addresses does Snowflake support for network policies?IPv4
How can you activate a network policy for an individual user in Snowflake?By setting the NETWORK_POLICY parameter for the user using ALTER USER
What is the benefit of rekeying data periodically?It ensures that data is encrypted with the latest security technology
What is the name of the schema that Snowflake automatically creates in every database in an account?INFORMATION_SCHEMA
What error is returned if the filters specified in an Information Schema query are not sufficiently selective?Information schema query returned too much data. Please repeat query with more selective predicates
What is the difference between the ACCOUNT_USAGE and READER_ACCOUNT_USAGE views?ACCOUNT_USAGE views provide detailed metadata and usage metrics specific to your account, while the READER_ACCOUNT_USAGE views offer similar but limited information focused on all associated reader accounts.
What is the retention period of the ACCOUNT_USAGE views that display historical usage metrics?1 year
What is the name of the view that provides user access history in Snowflake?ACCESS_HISTORY
What is the name of the column that records the DDL operations on database objects in the ACCESS_HISTORY view?OBJECT_MODIFIED_BY_DDL
What is the difference between a full Snowflake account and a reader account in terms of data sharing?a full Snowflake account has the capability to both share and receive data, while a reader account is limited to only consuming data shared by its provider account
What are the three options for sharing data in Snowflake?a listing, which catalogs shared objects, a direct share, which allows secure access to specific data, and a data exchange, which facilitates data trading between different organizations
What is the main purpose of Data Exchange?a Data Exchange in Snowflake serves as a secure platform where a defined group of members can collaborate and share data effectively, facilitating controlled access and interaction around shared information.
What is the name of the feature that allows you to create trial accounts with selected Snowflake business partners and integrate them with Snowflake?Partner Connect
Which of the following objects are not replicated with database replication? PIPE,account parameters, privileges granted on database objects
What is the main advantage of Secure Data Sharing in Snowflake?consumers can only access the shared data without the ability to alter or delete it, ensuring data integrity and security for the provider. 
Which of the following languages is not supported by a Snowflake driver?pascal. it supports Go, c#, Java
How can you control the flow of execution with conditional statements in Snowflake Scripting?IF-ELSE,CASE
What is the main purpose of Snowpark?Snowpark is designed to empower developers to use their preferred programming languages, such as Python or Java, directly within the Snowflake environment, enhancing flexibility and integration in data processing tasks.
Which of the following actions can a user with the ORGADMIN role perform? (Choose 2) Create an account in the organization, Enable database replication for an account in the organization
How can you add a directory table to a stage? (Choose 2)By using CREATE STAGE with the DIRECTORY_TABLE option, By using ALTER STAGE with the DIRECTORY_TABLE option
What is the main difference between Snowflake and traditional database technologies or big data platforms?Snowflake uses a hybrid of shared-disk and shared-nothing architectures1
What is the default value of the ON_ERROR option in the COPY INTO <table> command?ABORT_STATEMENT
In Snowsight, Are views visible directly under the INFORMATION_SCHEMA?Yes, only the views are visible directly under INFORMATION_SCHEMA
Which SQL commands can you use to work with directory tables? (multiple answers) ALTER STAGE, CREATE STAGE
Which of the following operations require a warehouse to be running and in use for the session? Loading data into tables using DML operations, Executing SQL SELECT statements that require compute resources
Which of the following database objects can be shared with other Snowflake account?Secure Materialized View, Secure Views, Tables
How can you add search optimization for a specific column and a specific search method?Use ALTER TABLE … ADD SEARCH OPTIMIZATION ON <method>(<column>) *
Which of the following statements are true about network policies? (Choose two)Network policies can be created by any user with sufficient privileges.Network policies support only IPv4 addresses
What are some examples of data that consumers might use from the Snowflake Marketplace?Up-to-date streaming data, such as current weather and traffic conditions.Specialized identity data for understanding subscribers and audience targets,Historical data for research, forecasting, and machine learning
Which of the following constraints are always enforced by SnowflakeNOT NULL
How can you return recent execution times and other query metadata using the Information Schema?Use the QUERY_HISTORY table functions
What is the effect of adding 0.0.0.0/0 to the blocked IP address list in a network policy?It blocks all IPv4 addresses on the local machine.
Which of the following categories are included in the table of 3rd-party partners and technologies?Machine Learning, Data Integration, Data Visualization
What is the purpose of the query acceleration service?To improve overall warehouse performance, To reduce the impact of outlier queries, To accelerate parts of the query workload in a warehouse
Which of the following statements are true about Fail-safe for tables in Snowflake? (Select three)Fail-safe can only be accessed by Snowflake Support to recover data upon customer request.Fail-safe is automatically enabled for all permanent tables and cannot be disabled.Fail-safe is a feature that enables data recovery after it is no longer accessible through Time Travel
What type of objects does the Snowflake Information Schema contain?Table Function, Views
What is the syntax for returning the ID of the first query executed in the current session using LAST_QUERY_ID?LAST_QUERY_ID(1)
Which of the following properties are part of a customized schedule for a resource monitor? (Choose three)Start timestamp, End timestamp, Frequency
What is the name of the aggregate function that returns a MinHash state containing a MinHash array of length k?MINHASH
What is the name of the data structure that the search optimization service creates and maintains for each table?Search access path
Which of the following methods can be used to log in with MFA instead of using the push notification? (Choose two)Enter a Passcode, Call Me
What is the main purpose of the MinHash scheme?To compare sets without computing the intersection or union
What are the two ways to advance the offset of a stream to the current table version without consuming the change data in a DML operation?Recreate the stream or insert the current change data into a temporary table.
What is the difference between BERNOULLI and SYSTEM sampling methods?BERNOULLI includes each row with a probability of p/100, while SYSTEM includes each block of rows with a probability of p/100
Which languages are currently supported by Snowpark libraries?Java, Python, Scala
Which of the following compression types are supported by the SOURCE_COMPRESSION option in the PUT command?BROTLI, GZIP, BZ2
Which of the following statements are true about unstructured data in Snowflake? (Choose all that apply)You can use Snowsight to click on a generated scoped, pre-signed, or file URL and download the referenced file, You can use server-side encryption when you create an internal stage with SNOWFLAKE_SSE encryption type, Both external and internal stages support unstructured data
How does Snowflake leverage clustering metadata to avoid unnecessary scanning of micro-partitions?By pruning the micro-partitions that do not match the filter predicates
Which of the following statements are true about the result cache layer? (Choose two)It is invalidated by the current_time() function,It is available across virtual warehouses
What is the purpose of a user-defined function (UDF) in Snowflake?To call a function from SQL and manipulate data within the constraints of the handler language, To extend the system with operations that are not available through the built-in functions, To encapsulate functionality so that it can be called repeatedly from multiple places in code
Which two methods can be used to view data storage for individual tables in Snowflake?TABLE_STORAGE_METRICS view, SHOW TABLES command
Which of the following categories of time spent can be displayed in the Profile Overview?Remote Disk IO, Initialization, Local Disk IO
What is the name of the schema that contains the Snowflake Access History View? ACCOUNT_USAGE
Which schema contains views related to the execution times of queries and tasks?ACCOUNT_USAGE
Which of the following privileges are required for roles other than account administrators to view and modify resource monitors using SQL? (Choose2)MONITOR,MODIFY
Which of the following factors affect the storage charges that Snowflake bills your account for using tables?The Fail-safe period for the table, The table type (permanent, transient, or temporary), The Time Travel retention period for the table
Which of the following keywords are used to clone an object as of a specified time or point in the past?AT, BEFORE, STATEMENT
Which of the following statements are true about the PUBLIC role? (Choose 3)It is typically used when explicit access control is not needed.It can own securable objects.It is automatically granted to every user and role in the account.
Which of the following statements are true about re-clustering a table in Snowflake? (Choose two)Reclustering consumes credits and results in storage costs, Reclustering co-locates similar rows in the same micro-partitions.
















 





 
























