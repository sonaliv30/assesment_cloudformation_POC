#OpenSupports Infrastructure Setup Using AWS CloudFormation
This repository contains the infrastructure setup for the OpenSupports application using AWS CloudFormation. The application has been deployed across three environments: development, staging, and production, using parameterized templates to manage each environment's isolated infrastructure.


Setup Prerequisites
Before starting, ensure the following prerequisites are met:

1.Fork the OpenSupports Repository: Fork the official OpenSupports GitHub repository into your GitHub account to modify and integrate with your infrastructure.

2.AWS Account: You must have an active AWS account with appropriate permissions to create and manage AWS resources like VPCs, EC2 instances, RDS, and more.

3.AWS CLI and Git: Make sure the AWS CLI and Git are installed and configured.

4.Key Pair: Ensure you have an SSH key pair set up in AWS for EC2 access.

Architecture:
The OpenSupports application is deployed across three isolated environments (development, staging, and production). Each environment consists of its own isolated resources:

VPC: A dedicated Virtual Private Cloud for each environment.
Subnets: Public and private subnets to host EC2 instances and RDS.
EC2 Instances: To host the OpenSupports application.
RDS (MySQL): A database for the application, using separate instances for each environment.
S3 Bucket: For storing static files like user uploads, logs, and backups.

Best Practices: 
Security: Implement IAM Roles with least privilege, secure DB credentials using AWS Secrets Manager, and enforce encrypted communication using SSL.
High Availability: Enable Multi-AZ for production databases and use Auto Scaling Groups for EC2 instances.
Monitoring: Use CloudWatch for detailed monitoring of EC2, RDS, and application logs.

##Parameters Section:

The DBUser and DBPassword are defined as parameters in your CloudFormation template. This means they are values that you can provide at the time of stack creation.
DBPassword has the property NoEcho: true, which ensures that the password will not be visible in the AWS Management Console or in the CloudFormation events logs for security reasons.

Cost Optimization :
Spot Instances: Use Spot Instances in non-production environments to reduce EC2 costs.
Auto Scaling: Configure Auto Scaling Groups to dynamically adjust the number of EC2 instances based on traffic.
Instance Sizing: Use appropriate instance sizes for development (t2.micro) and production (t3.medium).

