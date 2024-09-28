# assesment_cloudformation_POC

##Parameters Section:

The DBUser and DBPassword are defined as parameters in your CloudFormation template. This means they are values that you can provide at the time of stack creation.
DBPassword has the property NoEcho: true, which ensures that the password will not be visible in the AWS Management Console or in the CloudFormation events logs for security reasons.
