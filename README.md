#OpenSupports Infrastructure Setup Using AWS CloudFormation
This repository contains the infrastructure setup for the OpenSupports application using AWS CloudFormation. The application has been deployed across three environments: development, staging, and production, using parameterized templates to manage each environment's isolated infrastructure.

##Parameters Section:

The DBUser and DBPassword are defined as parameters in your CloudFormation template. This means they are values that you can provide at the time of stack creation.
DBPassword has the property NoEcho: true, which ensures that the password will not be visible in the AWS Management Console or in the CloudFormation events logs for security reasons.
