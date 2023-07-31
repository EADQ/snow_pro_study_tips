# COMPUTE_LAYER

## Virtual Warehouses

### A named wrapper around a cluster of servers with CPU, memory, and disk.
### The larger the warehouse, the more servers in the cluster.
### An extra-small WH has one server per cluster.
#### Each size up doubles in size.
### Jobs requiring compute resources run on virtual warehouses.
### Running a virtual warehouse consumes Snowflake credits.
### Storage and compute resources scale independently.

## Three Types of Compute

### Compute provisioned by you:
#### Virtual Warehouse Compute 
#### Run on virtual warehouses that you create, resume and suspend.
#### May be auto-resumed or auto-suspended.
#### Billed per second with a one-minute minimum.

### Compute provisioned by Snowflake:
##### Compute for Serverless Features 
###### Billed per second with no minimum. 
###### Used for specific features (for example, Snowpipe, clustering service, and Tasks).

#### Cloud Services Compute
##### Used for things like cache lookups and cloning tables.
##### Billed per second with no minimum.
##### Only charged for any amount that exceeds 10% of total compute usage.

### VIRTUAL WAREHOUSE SIZING

#### Warehouses are sized in "t-shirt" sizing (XS, S, M, L, etc.).
#### Can be resized at any time, even when running. New queries will run with the new WH size.
#### Size determines the number of servers that comprise each cluster in a warehouse.
#### Each larger size is double the preceding, in both VMs in the cluster and in Snowflake credits consumed.
#### To facilitate start-up times, there is a pool of running servers ready to go to reduce or eliminate start-up time when resuming a virtual warehouse.

#### Warehouses can be resized using ALTER WAREHOUSE statement or the UI.
#### USE ALTER WAREHOUSE WAIT FOR COMPLETION = TRUE to ensure all required compute resources
#### are fully provisioned for a warehouse before it is available at the new size.
##### The value of this parameter is not persisted so must be set where desired.
#### Effects of resizing:
##### A suspended warehouse will start at new size upon next resume
##### Running Warehouse: immediate impact; running queries complete at current size, while queued queries run at new size.

## VIRTUAL WAREHOUSE TYPES
### Standard
#### Will only ever have a single compute cluster.
#### Cannot "scale out"

### Multi-Cluster Warehouse (MCW)
#### Can spawn additional compute clusters (scale out) <br>to manage changes in user demand and concurrency issues.
#### Enterprise Edition feature.

## SCALING UP VS. SCALING OUT

### SCALING UP
#### Resizing a warehouse to handle COMPLEX / process-intensive queries.

### SCALING OUT
#### Adding more clusters to your current Virtual <br>Warehouse without changing the size of the
#### Warehouse to handle CONCURRENCY issues.

## Scale Up for Performance

### Elastic Processing Power (CPU, RAM, SSD)
#### Raw performance boost for complex queries or large data sets.
#### Complex queries on large datasets require larger warehouses.
#### Not intended for handling concurrency issues (more users/queries.

### Warehouse Sizing Guidelines
#### Snowflake uses per-second billing:use larger <br>warehouse for more complex <br>workloads and (auto) suspend when not in use.
#### Keep queries of similar size and complexity <br>on the same warehouse to simplify compute resource sizing.

## Scale Out for Concurrency

### General Functionality and Considerations
#### Single virtual warehouse with multiple compute clusters.
#### Delivers consistent SLA, automatically adding and removing compute clusters based on concurrent usage.
#### Scale out during peak demand and scale in when there's low demand.
#### Queries are load balanced across the clusters in a virtual warehouse.
#### Deployed across availability zones for high availability.

### Guidelines
#### MIN CLUSTER COUNT: 1-10 (default 1)
#### MAX CLUSTER COUNT: 1-10 (default 1) >=
#### MIN CLUSTER COUNT

## Compute Credits

#### Determine how you're billed for compute usage
##### You may have a set number of credits.
##### You may be billed monthly for your credits.
#### Charge based on the number of virtual <br>warehouses you use, their size, and how long they run.
#### Warehouse usage (or compute) is charged <br>per-second, with a one-minute minimum.