# Storage - S3 - Components - Bucket
- Access style:
  - Virtual-hosted-url: http://bucket.s3.amazonaws.com or http://bucket.s3-aws-region.amazonaws.com 
  - Path style url: http://s3.amazonaws.com/bucket or https://s3-aws-region.amazonaws.com/bucket 
- Buckets are the mains storage container of S3, and contain a grouping of information and have sub namespaces that are similar to folders
- Tags can be used to organize buckets
- Each bucket must have a unique name across all of AWS
- Limitations:
  - 100 buckets per AWS at a time
  - Bucket ownership cannot be transferred once a bucket is created