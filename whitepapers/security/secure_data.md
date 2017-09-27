# Secure data

Resource access authorization
Using resource and capability policies which are cumulative in nature.
Storing and managing encryption keys in the cloud
You can use on-premises HSMs or CloudHSM to support a variety of use cases and applications, such as database encryption, Digital Rights Management, and Public Key Infrastructure (PKI) including authentication and authorization, document signing, and transaction processing. CloudHSM currently uses Luna SA HSMs from SafeNet.

When you sign up for CloudHSM, you receive dedicated single tenant access to CLoudHSM appliances. Each appliance appears as a resource in your Amazon VPC. You, not AWS, initialize and manage the cryptographic domain of the CloudHSM. AWS admins manage, maintain, and monitor health of the CloudHSM appliance.

You can implement CloudHSMs in multiple AZ with replication between them to provide high availability and storage resilience.

Protecting data at rest
Amazon S3 provides a number of security features for protection of data at rest, which you can use or not depending of your threat profile:
Permission
Versioning
Replication: Replicates each object across all AZs within the respective region.
Backup: Replication + Versioning (on-premise backup)
Encryption-server side: AES-256
Encryption-client side

Amazon EBS is the AWS abstract block storage service. Features for protecting it:
Replication: AWS creates two copies of the EBS volume for redundancy (same AZ)
Backup: AWS provides snapshots to capture the data stored on an EBS volume at a specific point in time.
Encryption: Microsoft Windows EFS (Encrypted File System)
Encryption: Microsoft: BitLocker is a volume encryption solution. AES 128 and 256 bit encryption.
Encryption: Linux dm-crypt
Encryption: TrueCrypt: Third party tool for Windows and Linux
Encryption and integrity authentication: SAfeNEt ProtectV: It is a third-party offering that allows for full disk encryption of Amazon EBS volumes and pre-boot authentication of AMIs. It provides data confidentiality and data integrity authentication for data and the underlying operating system.

Amazon RDs leverages the same secure infrastructure as Amazon EC2. You can add protection at the application layer, for example, using a built-in encryption function that encrypts all sensitive database fields, using an application key, before storing the data in the database.

All data stored in Amazon Glacier is protected using server-side encryption (AES-256).

DynamoDB supports number, string, and raw binary data type formats. When storing encrypted fields in DynamoDB, it is a best practice to use a raw binary fields or Base64-encoded string fields.

Amazon EMR is a managed service in the cloud. AWS provides the AMIs required to run the Amazon EMR, and you can’t use custom AMIs or your own EBS volumes. By default, Amazon EMR instances do not encrypt data at rest. Encryption techniques:
Amazon S3 server-side encryption-no HDFS copy.
Amazon S3 client-side encryption
Application-level encryption-entire file encrypted
Application-level encryption-individual fields encrypted/structure preserved
Hybrid
Protecting data in transit
Services from AWS provide support for both IPSec and SSL/TLS for protection of data in transit.