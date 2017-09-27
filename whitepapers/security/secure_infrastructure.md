# Secure infrastructure

- On AWS, you can build network segments using the following access control methods:
  - VPC: To define an isolated network for each workload or organizational entity.
  - Security groups: To manage access to instances that have similar functions and security requirements; they are stateful firewalls that enable firewall rules in both directions. TCP or UDP
  - Network Access Control List: Stateless management of IP traffic. They are agnostic to TCP or UDP sessions. 
  - Host-based firewalls
  - Threat protection layer
  - Access control at other layers (applications and services)
- Creating a security zone requires additional controls per network segment, and they often include:
  - Shared access control: Central identity access management system (IDAM)
  - Shared audit logging
  - Shared data classification
  - Shared management infrastructure
  - Shared security requirements