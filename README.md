# aws-cloudformation
This project represents a template that is made for the AWS CloudFormation service.

1. Create a IAM-Role called 'UdagramS3ReadOnlyEC2'
 -  Policy Name: `AmazonS3ReadOnlyAccess`
 -  Trusted entities: `ec2`
2. Deploy the network template
 - `aws cloudformation create-stack --stack-name udagram-network --template-body file://network.yml  --parameters file://network-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=eu-central-1`
3. Deploy the server template
 - `aws cloudformation create-stack --stack-name udagram-servers --template-body file://servers.yml  --parameters file://servers-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=eu-central-1`
## Website
http://udagram-475271618.eu-central-1.elb.amazonaws.com
