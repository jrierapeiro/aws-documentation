- When you create a VPC, it spans all of the AZs in the region. After creating a VPC, you can add one or more subnets in each AZ. Each subnets must reside entirely within one AZ and cannot span zones.
- Subnets must be associated with a route table
- A public subnet has a route to the internet (RT with IGW)
- A private subnet does not have a route to the internet(RT without IGW)
- Minimum size /28 max size /16 (from 16 IPs to  65536 Ips)
- You cannot delete a subnet with running instances
- Reserved IPs
  - 10.0.0.0: Network address.
  - 10.0.0.1: Reserved by AWS for the VPC router.
  - 10.0.0.2: Reserved by AWS. The IP address of the DNS server is always the base of the VPC network range plus two; however, we also reserve the base of each subnet range plus two. 
  - 10.0.0.3: Reserved by AWS for future use.
  - 10.0.0.255: Network broadcast address. We do not support broadcast in a VPC, therefore we reserve this address.
