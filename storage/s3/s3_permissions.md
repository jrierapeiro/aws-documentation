# Storage - S3 - Permissions

- All buckets and objects are private by default (only owner access)
- The resource owner can grant access to the resource through S3 resource based policies or access can be granted through a traditional IAM user policy
- Resource based policies:
  - Bucket policies:
    - Attached only to the S3 bucket
    - Permission applied to all objects in the bucket
    - Actions allowed or denied
  - S3 access control lists:
    - Grant access to users in other AWS accounts or to the public
    - Both buckets and objects has ACLs
    - Object ACLs allow us to share an S3 object with the public via a URL link