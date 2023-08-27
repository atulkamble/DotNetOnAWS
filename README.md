# DotNetOnAWS
## Publish as ASP.NET Core App to AWS Elastic Beanstalk on Linux
To successfully publish .NET applications to an AWS service, install the following to your local device:
## Prerequisites

1. .NET Core 3.1+(which includes .NET5 and .NET6): https://dotnet.microsoft.com/en-us/download
2. Node.js 14.x or later version: Node.js is required to run AWS Cloud Development Kit (AWS CDK). https://nodejs.org/en/download
3. (Optional) Docker is used when deploying to a container-based service such as Amazon ECS. https://docs.docker.com/get-docker/

# Confirmed Stack
http://dotnetonaws-dev.eba-6pmrbcah.us-east-1.elasticbeanstalk.com/

# Services
EC2, IAM (Access key, secret access key, S3:Buckets(policy*), AWS CloudFormation, Amazon Elastic Beanstalk

- Created depolyment zip bundle
Creating Dotnet Publish Zip file...
Using self contained publish since AWS Elastic Beanstalk does not currently have .NET 7 preinstalled
MSBuild version 17.6.10+2679cf5a9 for .NET
  Determining projects to restore...
  Restored D:\Github\DotNetOnAWS\DotNetOnAWS\DotNetOnAWS.csproj (in 20.74 sec).
  DotNetOnAWS -> D:\Github\DotNetOnAWS\DotNetOnAWS\bin\Release\net7.0\linux-x64\DotNetOnAWS.dll
  DotNetOnAWS -> C:\Users\Admin\AppData\Local\Temp\4df0ddb1-0558-47e0-963a-1ab69df80d4b\

- Configuring AWS Developement Kit
  Generating AWS Cloud Development Kit (AWS CDK) deployment project
Using bootstrapping template from C:\Users\Admin\.aws-dotnet-deploy\CDKBootstrapTemplate.yaml
 ⏳  Bootstrapping environment aws://316290926278/us-east-1...
Trusted accounts for deployment: (none)
Trusted accounts for lookup: (none)
Using default execution policy of 'arn:aws:iam::aws:policy/AdministratorAccess'. Pass '--cloudformation-execution-policies' to customize.
CDKToolkit: creating CloudFormation changeset...
CDKToolkit |  0/12 | 4:19:14 am | REVIEW_IN_PROGRESS   | AWS::CloudFormation::Stack | CDKToolkit User Initiated
CDKToolkit |  0/12 | 4:19:23 am | CREATE_IN_PROGRESS   | AWS::CloudFormation::Stack | CDKToolkit User Initiated
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::ECR::Repository    | ContainerAssetsRepository 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::S3::Bucket         | StagingBucket 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | LookupRole 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | ImagePublishingRole 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | CloudFormationExecutionRole 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::SSM::Parameter     | CdkBootstrapVersion 
CDKToolkit |  0/12 | 4:19:26 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | FilePublishingRole 
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | FilePublishingRole Resource creation Initiated
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | CloudFormationExecutionRole Resource creation Initiated
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | ImagePublishingRole Resource creation Initiated
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | LookupRole Resource creation Initiated
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::S3::Bucket         | StagingBucket Resource creation Initiated
CDKToolkit |  0/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::ECR::Repository    | ContainerAssetsRepository Resource creation Initiated
CDKToolkit |  1/12 | 4:19:27 am | CREATE_COMPLETE      | AWS::ECR::Repository    | ContainerAssetsRepository 
CDKToolkit |  1/12 | 4:19:27 am | CREATE_IN_PROGRESS   | AWS::SSM::Parameter     | CdkBootstrapVersion Resource creation Initiated
CDKToolkit |  2/12 | 4:19:28 am | CREATE_COMPLETE      | AWS::SSM::Parameter     | CdkBootstrapVersion 
CDKToolkit |  3/12 | 4:19:42 am | CREATE_COMPLETE      | AWS::IAM::Role          | FilePublishingRole 
CDKToolkit |  4/12 | 4:19:42 am | CREATE_COMPLETE      | AWS::IAM::Role          | ImagePublishingRole 
CDKToolkit |  5/12 | 4:19:42 am | CREATE_COMPLETE      | AWS::IAM::Role          | CloudFormationExecutionRole 
CDKToolkit |  6/12 | 4:19:43 am | CREATE_COMPLETE      | AWS::IAM::Role          | LookupRole 
CDKToolkit |  6/12 | 4:19:44 am | CREATE_IN_PROGRESS   | AWS::IAM::Policy        | ImagePublishingRoleDefaultPolicy 
CDKToolkit |  6/12 | 4:19:45 am | CREATE_IN_PROGRESS   | AWS::IAM::Policy        | ImagePublishingRoleDefaultPolicy Resource creation Initiated
CDKToolkit |  7/12 | 4:19:48 am | CREATE_COMPLETE      | AWS::S3::Bucket         | StagingBucket 
CDKToolkit |  7/12 | 4:19:48 am | CREATE_IN_PROGRESS   | AWS::IAM::Policy        | FilePublishingRoleDefaultPolicy 
CDKToolkit |  7/12 | 4:19:49 am | CREATE_IN_PROGRESS   | AWS::S3::BucketPolicy   | StagingBucketPolicy 
CDKToolkit |  7/12 | 4:19:49 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | DeploymentActionRole 
CDKToolkit |  7/12 | 4:19:49 am | CREATE_IN_PROGRESS   | AWS::IAM::Role          | DeploymentActionRole Resource creation Initiated
CDKToolkit |  7/12 | 4:19:49 am | CREATE_IN_PROGRESS   | AWS::S3::BucketPolicy   | StagingBucketPolicy Resource creation Initiated
CDKToolkit |  8/12 | 4:19:50 am | CREATE_COMPLETE      | AWS::S3::BucketPolicy   | StagingBucketPolicy 
CDKToolkit |  8/12 | 4:19:50 am | CREATE_IN_PROGRESS   | AWS::IAM::Policy        | FilePublishingRoleDefaultPolicy Resource creation Initiated
CDKToolkit |  9/12 | 4:20:00 am | CREATE_COMPLETE      | AWS::IAM::Policy        | ImagePublishingRoleDefaultPolicy 
CDKToolkit | 10/12 | 4:20:05 am | CREATE_COMPLETE      | AWS::IAM::Role          | DeploymentActionRole 
CDKToolkit | 11/12 | 4:20:05 am | CREATE_COMPLETE      | AWS::IAM::Policy        | FilePublishingRoleDefaultPolicy 
CDKToolkit | 12/12 | 4:20:07 am | CREATE_COMPLETE      | AWS::CloudFormation::Stack | CDKToolkit 
 ✅  Environment aws://316290926278/us-east-1 bootstrapped.



- Deploying AWS Project
✨  Synthesis time: 128.65s

DotNetOnAWS: building assets...

[0%] start: Building 1bddf49e012b1adccdce45490d79b5135e7e8c38bd0703802774ce6c35f1aa3f:316290926278-us-east-1
[0%] start: Building e9b224d20260a79b8b88996db78333249f9df40c8cb0cf1715f1e877d5f2dfeb:316290926278-us-east-1
[50%] success: Built 1bddf49e012b1adccdce45490d79b5135e7e8c38bd0703802774ce6c35f1aa3f:316290926278-us-east-1
[100%] success: Built e9b224d20260a79b8b88996db78333249f9df40c8cb0cf1715f1e877d5f2dfeb:316290926278-us-east-1

DotNetOnAWS: assets built

DotNetOnAWS: deploying...
[0%] start: Publishing 1bddf49e012b1adccdce45490d79b5135e7e8c38bd0703802774ce6c35f1aa3f:316290926278-us-east-1
[0%] start: Publishing e9b224d20260a79b8b88996db78333249f9df40c8cb0cf1715f1e877d5f2dfeb:316290926278-us-east-1
[50%] success: Published e9b224d20260a79b8b88996db78333249f9df40c8cb0cf1715f1e877d5f2dfeb:316290926278-us-east-1
[100%] success: Published 1bddf49e012b1adccdce45490d79b5135e7e8c38bd0703802774ce6c35f1aa3f:316290926278-us-east-1
DotNetOnAWS: creating CloudFormation changeset...
DotNetOnAWS | 0/8 | 4:23:19 am | REVIEW_IN_PROGRESS   | AWS::CloudFormation::Stack                | DotNetOnAWS User Initiated
DotNetOnAWS | 0/8 | 4:23:27 am | CREATE_IN_PROGRESS   | AWS::CloudFormation::Stack                | DotNetOnAWS User Initiated
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::Application        | Recipe/BeanstalkApplication (RecipeBeanstalkApplication3558EA83) 
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::IAM::Role                            | Recipe/BeanstalkServiceRole (RecipeBeanstalkServiceRole62B7EC28) 
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::IAM::Role                            | Recipe/AppIAMRole (RecipeAppIAMRole9E73EEFA) 
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::CDK::Metadata                        | CDKMetadata/Default (CDKMetadata) 
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::IAM::Role                            | Recipe/AppIAMRole (RecipeAppIAMRole9E73EEFA) Resource creation Initiated
DotNetOnAWS | 0/8 | 4:23:30 am | CREATE_IN_PROGRESS   | AWS::IAM::Role                            | Recipe/BeanstalkServiceRole (RecipeBeanstalkServiceRole62B7EC28) Resource creation Initiated
DotNetOnAWS | 0/8 | 4:23:31 am | CREATE_IN_PROGRESS   | AWS::CDK::Metadata                        | CDKMetadata/Default (CDKMetadata) Resource creation Initiated
DotNetOnAWS | 1/8 | 4:23:31 am | CREATE_COMPLETE      | AWS::CDK::Metadata                        | CDKMetadata/Default (CDKMetadata) 
DotNetOnAWS | 1/8 | 4:23:31 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::Application        | Recipe/BeanstalkApplication (RecipeBeanstalkApplication3558EA83) Resource creation Initiated
DotNetOnAWS | 2/8 | 4:23:37 am | CREATE_COMPLETE      | AWS::ElasticBeanstalk::Application        | Recipe/BeanstalkApplication (RecipeBeanstalkApplication3558EA83) 
DotNetOnAWS | 2/8 | 4:23:37 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::ApplicationVersion | Recipe/ApplicationVersion (RecipeApplicationVersion145C922C) 
DotNetOnAWS | 2/8 | 4:23:39 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::ApplicationVersion | Recipe/ApplicationVersion (RecipeApplicationVersion145C922C) Resource creation Initiated
DotNetOnAWS | 3/8 | 4:23:45 am | CREATE_COMPLETE      | AWS::ElasticBeanstalk::ApplicationVersion | Recipe/ApplicationVersion (RecipeApplicationVersion145C922C) 
DotNetOnAWS | 4/8 | 4:23:46 am | CREATE_COMPLETE      | AWS::IAM::Role                            | Recipe/AppIAMRole (RecipeAppIAMRole9E73EEFA) 
DotNetOnAWS | 5/8 | 4:23:46 am | CREATE_COMPLETE      | AWS::IAM::Role                            | Recipe/BeanstalkServiceRole (RecipeBeanstalkServiceRole62B7EC28) 
DotNetOnAWS | 5/8 | 4:23:47 am | CREATE_IN_PROGRESS   | AWS::IAM::InstanceProfile                 | Recipe/Ec2InstanceProfile (RecipeEc2InstanceProfileB2CA3751) 
DotNetOnAWS | 5/8 | 4:23:48 am | CREATE_IN_PROGRESS   | AWS::IAM::InstanceProfile                 | Recipe/Ec2InstanceProfile (RecipeEc2InstanceProfileB2CA3751) Resource creation Initiated
5/8 Currently in progress: DotNetOnAWS, RecipeEc2InstanceProfileB2CA3751
DotNetOnAWS | 6/8 | 4:25:59 am | CREATE_COMPLETE      | AWS::IAM::InstanceProfile                 | Recipe/Ec2InstanceProfile (RecipeEc2InstanceProfileB2CA3751) 
DotNetOnAWS | 6/8 | 4:26:00 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::Environment        | Recipe/BeanstalkEnvironment (RecipeBeanstalkEnvironment83CC12DE) 
DotNetOnAWS | 6/8 | 4:26:02 am | CREATE_IN_PROGRESS   | AWS::ElasticBeanstalk::Environment        | Recipe/BeanstalkEnvironment (RecipeBeanstalkEnvironment83CC12DE) Resource creation Initiated
6/8 Currently in progress: DotNetOnAWS, RecipeBeanstalkEnvironment83CC12DE
DotNetOnAWS | 7/8 | 4:28:07 am | CREATE_COMPLETE      | AWS::ElasticBeanstalk::Environment        | Recipe/BeanstalkEnvironment (RecipeBeanstalkEnvironment83CC12DE) 
DotNetOnAWS | 8/8 | 4:28:08 am | CREATE_COMPLETE      | AWS::CloudFormation::Stack                | DotNetOnAWS 

 ✅  DotNetOnAWS

✨  Deployment time: 341.17s

Stack ARN:
arn:aws:cloudformation:us-east-1:316290926278:stack/DotNetOnAWS/59d0eee0-4463-11ee-bcca-125bd53fa243

✨  Total time: 469.82s




DotNetOnAWS was published as ASP.NET Core App to AWS Elastic Beanstalk on Linux
  
