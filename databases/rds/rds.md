- OLTP: Online transaction processing
- RDS is a fully managed Relational Database System
  - Does not allow access to the underlying operating system
  - RDS provides vertical scaling (hardware)
  - Multi-AZ deployments for backup and high available solutions
    - It synchronously replicates data to a backup (standby) database instance located in another AZ (but in the same region)
    - In case of any failure: AWS will automatically switch the CNAME DNS record from the primary instance to the standby instance.
  - Read replicas (MySql/PostgreSQL/Aurora/MariaDB)
    - You can monitor replication lag using Cloudwatch
    - They allow elasticity in RDS
    - You can promote a read replica to a primary instance
    - MySQL: Can replicate across regions