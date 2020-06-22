# AWS-SAM-CLI bug
To reproduce:

```bash
cd sar/
# Modify makefile to point at s3 buckets you have permissions to in each region published
make bucket=... publish-us-east-1 # bucket in us-east-1
make bucket=... publish-us-east-2 # bucket in us-east-2
cd ../consumer
AWS_DEFAULT_REGION=us-east-2 sam build --debug # fails
AWS_DEFAULT_REGION=us-east-1 sam build --debug # succeeds
```
