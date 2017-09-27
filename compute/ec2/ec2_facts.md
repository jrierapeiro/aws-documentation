- A SG must be assigned to an instance during the creation process
- Each instance must be placed into an existing VPC, AZ and subnet
- Automated (bootstrapping) custom launch commands can be passed into the instance during launch via user-data scripts
  - View user-data and instance meta-data:
    - curl http://169.254.169.254/latest/user-data
    - curl http://169.254.169.254/latest/meta-data
- Tags can be used to name and organize instances
- Encrypted key-pairs are used to manage login authentication
- There are limits on the amount of instances you can have running in a region at any particular time
- 20 EC2 instances per Region for new AWS accounts. (submit increase)

- You can prevent an instance from being terminated accidentally by someone using the AWS Management Console, the CLI, and the API. This feature is available for both Amazon EC2 instance store-backed and Amazon EBS-backed instances. Each instance has a DisableApiTermination attribute with the default value of false (the instance can be terminated through Amazon EC2). You can modify this instance attribute while the instance is running or stopped (in the case of Amazon EBS-backed instances)
- Ec2 instance level: “The choice to not use dedicated tenancy at the VPC level., An IAM policy explicitly allowing a user the right to terminate all EC2 instances.” The default option for a VPC is to not use dedicated tenancy, but that can be overridden at the instance level. If the option to use dedicated tenancy is explicitly set at the VPC level, however, it cannot be overridden at the instance level. Explicit denies in IAM policies always trump explicit allows, so a user who is allowed to terminate all EC2 instances in an account can be denied the permission to terminate a particular instance.

