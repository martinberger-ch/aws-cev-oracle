# aws-cev-oracle
cloud Formation Templates for AWS Custom Engine Version for Oracle.

## codebuild-vpc-infra.yaml
Create the VPC infrastructure:
- Private & Public Subnet
- Internet Gateway
- NAT Gateway
- Two Route Tables (private & public)
- Two Security Groups (private & public)

The security group has a simple ruleset (public ingress by 22/SSH - full access inside private subnet)

## codebuild-vpc-endpoints.yaml
Create the CEV required endpoints and set the subnet / security group for:
- S3
- SSM Service
- EC2 
- etc.

## custom-oracle-iam.json
Create the CEV required IAM role to use the CEV service. From the AWS documentation-
