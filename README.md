# Snowflake-pro
What are the three key layers of Snowflake’s architecture? Storage Layer, processing layer and cloud services layer
What is the name of the new web interface for Snowflake? snowsight
How can you change your password or security role in Snowsight? by using the profile section
What are the two types of warehouses available in Snowflake? standard and snowpark optimized
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













