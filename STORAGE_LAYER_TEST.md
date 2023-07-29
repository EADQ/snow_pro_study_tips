# Storage_Layer_Test

## Who owns and manages the cloud storage layer hosted <br>on Cloud Providers?
### Snowflake
#### Comments: Snowflake owned and manages the Cloud Storage <br>layers for all the Snowflake services for all of its customers


## Snowflake Storage layer is a Cloud Storage layer. <br>It depends on which cloud provider you are using. The current available cloud providers
### Azure Cloud
### AWS Cloud
### GCP

## Which feature in snowflake allows you <br>to load data in micro batches?
### Snowpipe

## What is a micro-partition?
### A small file that stores part of a table, along with metadata <br>about what it contains, such as MIN, MAX, COUNT

## The following statements describes a <br>benefit of Snowflake's separation of compute and storage?
### Compute can be scaled up or down without the requirement to add more storage
### Storage expands without the requirement to add more compute
### Multiple compute clusters can access stored data without contention

## True: Storage can increase or decrease without any effect on virtual warehouse sizes
### Comments: Snowflake architecture is designed in such <br>a way that storage and compute can be independently increased or decreased without any impact on each other

## Which type of data incur snowflake storage cost?
### Data retained to enable data recovery(fail-safe and time travel)
### Data stored in permanent tables
#### Comments: Storage cost is charged for below type of data <br>1.Files stored in Snowflake locations (i.e. user and table stages or internal named stages) <br>for bulk data loading/unloading. The user who stages a file can choose whether or not to compress the file to reduce storage. <br>2. Data stored in database tables, including historical data maintained for Time Travel. <br>Snowflake automatically compresses all data stored in tables and uses <br>the compressed file size to calculate the total storage used for an account. <br>3. Historical data maintained for Fail-safe.

## In which of the following cases the metadata <br>can incur storage and compute costs?
### Replicating a clone table

## Which of these objects consumes both storage and compute?
### Materialized view