## CodeStar-Deploying-and-Changing-Serverless-Patterns

CodeStar Deploying and Changing Serverless Patterns

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/d1c4214d-4023-4d82-b4a0-5398b33b5eee)


AWS CodeStar can be used to create, manage and work with software development projects. It helps in developing, building, and deploying applications on AWS with an AWS CodeStar Project.


It brings togethers following AWS services-

AWS CodeCommit (Managed Git Source Code Repository)

AWS CodeBuild (Managed Build Service to build & test code)

AWS CodeDeploy (Automated Software Development)

AWS CloudFormation (Configuration Based Resource Creation)

AWS CodePipeline (Managed CI/CD Pipeline)


## AWS Developer tools for CI/CD

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/1b11632d-2649-469f-98fb-b525094418f7)

## Architecture Diagram

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/65d2121a-3d16-48aa-8437-f47b1123df73)

# 1-Create a Project in AWS CodeStar (MyProject)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/37a9893c-d3c1-4d1c-8da6-d6b17e2d18ca)

## Create service role

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/4e20d681-c7d1-4fa8-8b5a-58deabc55b3a)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/e8494e71-fb26-488c-81e5-0ddffadee1d4)

## Choose a project template

click on the Search bar present and Select AWS Lambda as AWS Service, Go Web service as the Application Type, and node.js in the Programming language.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/7d2be176-6f31-4815-883b-f6c8d8cfa61a)

## Set up your project:

Project name: Enter MyProject

Keep all the options as default and click on the Next button.

Select the repository provider. I select Github

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/fbdcbfb2-f4fd-4891-902f-9fcc59718f2a)

## Review everything and click on the Create project button

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/1194b43b-6ff8-4f9c-af21-da2732bed579)

Alternatively, you can check the resources getting created by CodeStar in the CloudFormation console.

Navigate to CloudFormation by clicking on the Services menu at the top, under the Management & Governance section.

Stack named codestar-webapp-go is getting created. Click on the Stack name to check out the resources and events.

Switch to Events, Resources then Parameters tab to know more.

Upon successful creation of stack named codestar-webapp-go, another stack will be created called as awscodestar-myproject-infrastructure

Check out their Events, Resources, and Parameters section too.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/bc0c928c-2321-435b-b738-366c71851788)


## Explore project resources created by CodeStar

Lambda function: It contains the logic of the web service, IAM Role, and 1 IAM Policy, CodePipeline pipeline, CodeDeploy application and CodeDeploy deployment group,

CodeCommit repository, CodeBuild Project, CloudFormation stack, Amazon S3 bucket, API in API Gateway.


![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/adc4a62b-73b1-4b37-bed7-a0e8cdc8972b)









