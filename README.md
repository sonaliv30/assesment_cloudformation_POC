#OpenSupports Infrastructure Setup Using AWS CloudFormation
This repository contains the infrastructure setup for the OpenSupports application using AWS CloudFormation. The application has been deployed across three environments: development, staging, and production, using parameterized templates to manage each environment's isolated infrastructure.


Setup Prerequisites
Before starting, ensure the following prerequisites are met:

1.Fork the OpenSupports Repository: Fork the official OpenSupports GitHub repository into your GitHub account to modify and integrate with your infrastructure.

2.AWS Account: You must have an active AWS account with appropriate permissions to create and manage AWS resources like VPCs, EC2 instances, RDS, and more.

3.AWS CLI and Git: Make sure the AWS CLI and Git are installed and configured.

4.Key Pair: Ensure you have an SSH key pair set up in AWS for EC2 access.

##Parameters Section:

The DBUser and DBPassword are defined as parameters in your CloudFormation template. This means they are values that you can provide at the time of stack creation.
DBPassword has the property NoEcho: true, which ensures that the password will not be visible in the AWS Management Console or in the CloudFormation events logs for security reasons.
