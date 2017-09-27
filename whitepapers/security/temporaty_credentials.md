# IAM Roles and temporary security credentials

- There are scenarios in which you want to delegate access to users or services that don’t normally have access to your AWS resources:
  - Applications running on Amazon EC2 instances that need to access AWS resources
  - Cross account access
  - Identity federation
- IAM roles and temporary security credentials address these use cases. IAM role lets you define a set of permissions to access the resources that a user o service need, but the permissions are not attached to a specific IAM user or group. Instead, IAM users, mobile and EC2-based applications, or AWS services can programmatically assume a role. Assuming the role returns temporary credentials that the user or application can use to make for programmatic requests to AWS.