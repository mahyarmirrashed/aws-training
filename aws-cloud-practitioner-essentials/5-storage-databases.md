# Module 5: Storage and Databases

## Instance Stores and Amazon Elastic Block Store

- Block-level storage: method to store files on disk
  - Efficient storage type for databases, enterprise software, or filesystems
- Some EC2 instances come with Instance Store Volumes
  - Physically attached to host EC2 instance runs off of
  - Stopping/terminating EC2 instance data deletes information held within instance store volume
  - Useful for temporary files, scratch data, or easily reproduceable data
- Amazon Elastic Block Store (EBS): EBS store volumes
  - Not attached to specific EC2 instances (persists between stops)
  - Ability to choose size, type, and volume configurations
- EBS allows taking snapshots (incremental backups) of stored data
  - Important to take regular snapshots of volumes
  - Ability to restore data from snapshots
- EBS only available across single Availability Zone to EC2 instances

## Amazon Simple Storage Service

- Amazon Simple Storage Service (S3) buckets: ability to store and retrieve unlimited amounts of data
- Stores data (up to 5TB) as objects within buckets
  - Ability to version objects (simple paper trail)
- Stage data between different tiers and control permissions
- Amazon S3 Standard: stores data in minimum of three Availability Zones
- Amazon S3 static website hosting
  - Upload HTML code and other assets, click checkbox to host as static website
- S3 Standard-Infrequent Access (IA): excellent for long-term storage
- Amazon S3 Glacier: auditing logs that are very rarely accessed and speed is not of critical consequence (best for archiving)
- Ability to establish WORM (write once/read many) policy forever on desired buckets
- S3 Lifecycle management: automatically move data between tiers of durability and access patterns
- Block storage allows delta updates (rather than updating entire file)

## Amazon Elastic File System

- Amazon EFS allows AWS to do heavy-lifting of scaling and replication
  - Multiple instances can access EFS data concurrently
- EFS is true Linux file system (allowing concurrent accesses)
- Regional resources for EC2 instances within same region
- Automatically scales based on usage

## Amazon Relational Database Service

- Relational data bases use structure query language (SQL)
- RDBMS: relational database management system
- Amazon supports many types of databases (e.g. MySQL, OracleDB)
- Amazon provides lift-and-ship migration tools
- Amazon RDS provides automated patching, backups, redundancy, failover, and disaster recovery
- Amazon Aurora: most managed database service offered by Amazon
  - Supports MySQL and PostgreSQL
  - 1/10th of commercial database cost
  - Automatic data replications (up to 15)
  - Continuous backup options to S3 buckets

## Amazon DynamoDB

- DynamoDB is a serverless NoSQL database (non-relational)
- Tables contains items with different attributes
- Query patterns should usually only operate on single tables
- Millisecond response time, fully managed, automatically scalable

## Amazon Redshift

- Data warehouses are optimized for historical analytics as opposed to operational analysis
- Data warehousing as a service

## AWS Database Migration Service

- Helps customers migrate existing databases onto AWS securely
- Launch migration task (performs migration asynchronously)
- AWS provides schema migration tool (for heterogeneous migration)
- Migration tools can be used for creating test databases for developers
- Database consolidation can merge multiple databases into single database
- Continuous database replication (useful for caching information globally)

## Additional Database Services

- Amazon Neptune: graph database solution
- Amazon Managed Blockchain: immutable ledger
- Amazon Quantun Ledger Database: items cannot be removed from audit log
- Amazon Elasticache allows for memcachd and Redis flavours of micro-second caching
- Amazon DynamoDB Accelerator (DAX): speeding up DynamoDB outputs
