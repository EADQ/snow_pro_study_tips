# Storage_Layer

## STORAGE LAYER

### Where your data is stored.
### Infinitely scalable.
### You pay only for the storage you use.
### Data is organized in micro-partitions, in hybrid columnar format.
### Micro-partitions are IMMUTABLE.
### Hybrid columnar storage.
### Automatic micro-partitioning.
### Natural data clustering and optimization.
### Native semistructured data support and optimization.
### All storage within Snowflake is billable (compressed).

## COLUMNAR COMPRESSION

### Ingestion automatically analyzes and compresses data into tables on load.
### The engine finds the optimal compression scheme for each data type.
### Columns grow and shrink independently.
### Significant performance benefit by reducing 1/0 and storage.

## MICRO PARTITIONS

### Physical data files that comprise Snowflake's logical tables.
### Automatically-created contiguous units of storage, partitioned on ingestion order
### Attempts to preserve natural data co-location
### Immutable - updates create new micro-partitions.
### Micro-partitions are generally:
#### 50 - 500 MB before compression.
#### ~16 MB after compression.
### Many micro-partitions per table.
### Services layer stores metadata about every micro-partition:
#### MIN/MAX (Range of values in each column)
#### Number of distinct values

## META DATA

### Snowflake automatically collects and maintains metadata <br>about tables and their underlying micro-partitions, including:
### Table level
#### Row count
#### Table size (in bytes)
#### File references and table versions
### Micro-partition column level:
#### Range of values
#### Number of distinct values
#### MIN and MAX values

## DATA STORAGE BILLING

### Billed for actual storage use
#### Daily average Terabytes per month
### On-demand pricing
#### Billed in areas for storage used
#### Around $40/Terabyte/month
#### Minimum monthly charge of $25
### Pre-Purchased Capacity
#### Billed up front with commitment to a certain capacity
#### Price varies on amount and cloud platform
#### Customer is notified at 70% of capacity