- It is a VPc component that allows communication between instances in your VPC and the internet.
- It is horizontally scaled, redundant and highly available.
- It imposes no availability risks or bandwidth constraints on your network traffic
- Provides NAT translation for instances that have a public IP addresses assigned 
- Rules:
  - Only 1 IGW can be attached to a VPC at a time
  - An IGW cannot be detached from a VPC while there are active AWS resources in the VPC
  - An IGW must be attached to a VPC if the resources inside the VPC need to connect to resources via open internet
- To enable access to of from the internet for instances in a VPC subnet, you must attach an IGW to your VPC, ensure that your subnet’s route table points to the IGW. ensure that instances in your subnet have a public IP address or Elastic IP address, and ensure that your Network ACLs and SG rules allow the relevant traffic to and from your instance.