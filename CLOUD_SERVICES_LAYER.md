# Cloud Services Layers
## SNOWFLAKE ARCHITECTURE: CLOUD SERVICES

### "Brain" of the service
### Manages and coordinates activities across Snowflake
### Runs on compute instances provisioned by Snowflake

## RESPONSIBLE FOR:

### Security o Encryption o Metadata
### Updates and patches
### Query optimization o Transaction control o Cache management
### Replication management
### Micro-partitioning

## INFRASTRUCTURE MANAGEMENT

### Centralized management for all storage.
### Manages compute resources.
### Transparent handling of online updates and patches.

## OPTIMIZER SERVICE

### SOL Optimizer
#### Cost-based optimization (CBO).
### Automatic JOIN order optimization
#### No user input or tuning required.
### Automatic statistics gathering.
### Pruning using metadata about micro-partitions.
### Also referred to as Query parsing and optimization.

## SECURITY

### Authentication
### Access control for shares
### Role based access control (RBAC)
### Encryption and key management

## TRANSACTIONS CONTROL
#### Transaction: a sequence of SQL statements that are processed as an atomic unit.
### Snowflake transactions are
### ACID-compliance.
#### Atomicity
#### Consistency
#### Isolation
#### Durability
### Can include both reads and writes.

## METADATA MANAGEMENT

### Stores metadata as data is loaded into the system.
### Handles queries that can be processed completely <br>from metadata (without compute resources).
### Used for Time Travel and
### Cloning.
### Every aspect of
### Snowflake architecture leverages metadata.

## CLOUD SERVICES COMPUTE BILLING

### Some compute occurs in the cloud services layer
### Customers are charged for cloud computing that exceed 10% <br>of the daily usage of compute resources for the account
### The METERING HISTORY view inside the
### SNOWFLAKE.ACCOUNT_USAGE schema will provide the number of credits used in the account.
### This information is also available in the WebUl.