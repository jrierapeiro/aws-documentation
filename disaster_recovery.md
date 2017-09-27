# Disaster recovery

- Recovery time objective (RTO): Time it takes after a disruption to restore operations back to its regular service level, as defined by the companies operational level agreement.
- Recovery point objective (RPO): Acceptable amount of data loss measured in time.
- Not only should you design for disaster recovery for your applications running on AWS, you can also use AWS as a disaster recovery solution for your on-premise applications or data. The AWS services used should be determined based off of the business RTO and RPO operational agreement.
- Pilot light: A minimal version of your production environment that is running on AWS. This allows for replication from on-premise servers to AWS, and in the event of a disaster the AWS environment spins up more capacity (elasticity/automatically) and DNS is switch from on-premise to AWS. It is important to keep up to date AMI and instance configurations if following pilot light protocol.
- Warm standby: Has a larger foot print than a pilot light setup, and would most likely be running business critical application in standby. This type of configuration could also be used as a test area for applications
- Multi-site solution: Essentially clones of your production environment, which can either be in the cloud or on-premise. Has an active-active configuration which means instances size and capacity are all running in full standby and can easily convert at the flip of a switch. Methods like this could also be used to load balance using latency based routing or route 53 failover in the event of an issue.
- Examples:
  - Elastic load balancer and auto scaling
  - Amazon EC2 VM import connector
  - AMIs with up to date configurations
  - Replication from on-premise database servers to RDS
  - Automate the increasing of resources in the event of disaster
  - Use AWS Import/Export to copy large amounts of data to speed up replication times
  - Route 53 DNS failover/latency based routing solutions
  - Storage gateway