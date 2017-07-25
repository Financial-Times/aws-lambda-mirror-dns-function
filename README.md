Provides AWS Lambda function to mirror DNS zone from on-premises DNS server to Route 53 private hosted zone. See https://aws.amazon.com/blogs/compute/powering-secondary-dns-in-a-vpc-using-aws-lambda-and-amazon-route-53-private-hosted-zones/ for more details.


# deploy: 
```aws lambda create-function --function-name mirror-dns-lambda --runtime python2.7 --role  arn:aws:iam::591668573055:role/Monitoring-Sync-Dns-Role  --timeout 60 --vpc-config SubnetIds=subnet-5c6a7704,subnet-36904151,subnet-103de159,SecurityGroupIds=sg-ce0e18b7,sg-b80f19c1 --memory-size 128 --description "DNS fun" --zip-file fileb://mirror-dns-lambda.zip --handler lambda_function.lambda_handler```
