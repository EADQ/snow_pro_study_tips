# Snowflake Connectors & Drivers:

## DEF
### Snowflake provides native programmatic interfaces that allow <br>users to build applications that connect to Snowflake.

## DRIVERS

### Snowflake allows a third-party tool that supports <br>standard JDBC or ODBC but you need to download the Snowflake-specific driver (JDBC or ODBC ) from <br>web UI to be able to connect to the Snowflake database

## DRIVERS OVERVIEW

### Go: Interfase for developing applications using Go.
### JDBC: JDBC type 4 driver. Requires a 64-bit environment and Java.
### .NET: Interfase to the Microsoft .NET framework for application development.
### Node.js: Native asynchoronous Node.js interfase to Snowflake.
### ODBS: Connection to Snowflake using ODBC-based client applications. 
### PHP PDO: Interfase for developing PHP operations. 

## CONNECTOR OVERVIEW

### Kafka: Reads data from Apache Kafka topics and <br>loads the data into Snowflake tables.
#### Open-source distributed event streaming platform.
#### Publish/subscribe architecture.
#### High-throughput
#### Low-latency
#### Durable platform for streaming data.
### Python: Interface for developing Python applications<br> that can connect to Snowflake and all perform standard operations.
### Spark: Allows Spark to read and write data from/into Snowflake.
### SOL API *:  REST API used to access and update data in<br> a Snowflake database. Develop custom applications and <br>integrations that perform queries and manage deployments.



## SNOWFLAKE CONNETOR FOR KAFKA

### The Snowflake Connector for Kafka ("Kafka connector') reads data <br>from one or more Apache Kafka topics and loads the data into a Snowflake table.
### A topic produces a stream of rows to be inserted into a table
### Each message contains 1 row
### Allows a many-to-many relationship between publishers and subscribers.

## What is Spark?
### A distributed processing system with support <br>for multiple programming styles
### Performs both batch processing and new workloads <br>(streaming, interactive queries, machine learning, etc.)
### Supports multiple APIs
### Connects to a wide variety of sources, including SOL and NoSOL systems

### Spark Connector
#### Open-source
#### Allows bi-directional movement of data between a Snowflake cluster and a Spark cluster
#### Process data on the Spark cluster, or push processing down to Snowflake
##### Best if processing happens close to the data
#### Spark cluster can be self-hosted, or hosted on a 3rd party provider

## Snowflake Scripting:
### Extension of Snowflake SOL that adds support for procedural logic.
### Can be used to write stored procedures and procedural code outside of a stored procedure.

## SOL API
### Submit SQL statements
### Check the status of the execution
### Cancel the execution