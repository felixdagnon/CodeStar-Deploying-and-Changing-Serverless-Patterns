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

# 1-Create a Project in AWS CodeStar using Github reopsitory

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/37a9893c-d3c1-4d1c-8da6-d6b17e2d18ca)

## Create service role

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/4e20d681-c7d1-4fa8-8b5a-58deabc55b3a)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/e8494e71-fb26-488c-81e5-0ddffadee1d4)

## Choose a project template

click on the Search bar present and Select AWS Lambda as AWS Service, Go Web service as the Application Type, and node.js in the Programming language.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/7d2be176-6f31-4815-883b-f6c8d8cfa61a)

## Set up your project:

Project name: Enter codestar-webapp-go

Keep all the options as default and click on the Next button.

Select the repository provider. I select Github

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/fbdcbfb2-f4fd-4891-902f-9fcc59718f2a)

## Review everything and click on the Create project button

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/1194b43b-6ff8-4f9c-af21-da2732bed579)

Alternatively, you can check the resources getting created by CodeStar in the CloudFormation console.

Navigate to CloudFormation by clicking on the Services menu at the top, under the Management & Governance section.

Stack named codestar-webapp-go is getting created. Click on the Stack name to check out the resources and events.

Switch to Events, Resources then Parameters tab to know more.

Upon successful creation of stack named codestar-webapp-go, another stack will be created called as codestar-webapp-go-infrastructure

Check out their Events, Resources, and Parameters section too.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/bc0c928c-2321-435b-b738-366c71851788)


## View the Web application

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/7410a9f2-e1e6-46e9-b69f-c9549f476b2a)

## Explore project resources created by CodeStar

Lambda function: It contains the logic of the web service, IAM Role, and 1 IAM Policy, CodePipeline pipeline, CodeDeploy application 

and CodeDeploy deployment group, CodeCommit repository, CodeBuild Project, CloudFormation stack, Amazon S3 bucket, API in API Gateway.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/adc4a62b-73b1-4b37-bed7-a0e8cdc8972b)

##  View the pipeline and differentes phases

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/aa46bb9b-9777-4810-8f31-3504da9e7ba3)



# 2-Create a Project in AWS CodeStar using Codecommit reopository

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/a4277040-a6c6-47c6-9e6b-bda282793540)

## Choose a project template

click on the Search bar present and Select AWS Lambda as AWS Service, Web service as the Application Type, and python in the Programming language.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/0992e4e4-bdce-45a9-af2a-0894018c9014)


## Set up your project:

Project name: Enter python-codestar-api

Keep all the options as default and click on the Next button.

Select the repository provider. I select Codecommit

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/3ae1e55d-b997-4b2d-a2e5-33048ddbc54f)





## Review everything and click on the Create project button

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/6b266854-9e4e-49c8-83e0-e47be272cbfa)


Alternatively, you can check the resources getting created by CodeStar in the CloudFormation console.

Navigate to CloudFormation by clicking on the Services menu at the top, under the Management & Governance section.

Stack named python-codestar-api is getting created. Click on the Stack name to check out the resources and events.

Switch to Events, Resources then Parameters tab to know more.

Upon successful creation of stack named codestar-webapp-go, another stack will be created called as python-codestar-api-infrastructure

Check out their Events, Resources, and Parameters section too.

Click Cloud9

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/011dc84f-3015-4ab8-b565-1fd9ce24cdf4)


## Setup Cloud9 workstation to edit project code

Scroll up and click on the Set up AWS Cloud9 button.

On the Create AWS Cloud9 Environment details page,

Instance type: Select t2.micro

VPC: Select default VPC

Subnet: Select any subnet

Environment name: Enter demo

Environment description: Cloud9 environment for editing project code

Cost-saving settings: Select After 1 hour

Click on the Create environment button.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/0e517855-fb95-4ea2-afea-0fdea7fdb5fb)


It may take up to 5 minutes for creating the Cloud9 environment,

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/c904cca1-1963-483e-896a-5a26d6ce4879)


 you can check the same in the CloudFormation console. In the mean time, let’s check in the CloudFormation console.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/8f97d9e7-aeb1-4565-a459-32401430a95b)


After 5 minutes, you can see the status as CREATE_COMPLETE.

Go back to the codestar console, switch to the IDE tab, and refresh the page. Upon refreshing, you can see a demo environment is present, click on the Open IDE button.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/f2c4bab0-c4b3-4f1f-addf-e3845638efb7)


Cloud9 will prepare the environment for you, within few moments, you can see the CodeCommit repository getting cloned.

If your Cloud9 page is the same as shown in the below screenshot, you are ready for the next task.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/d24d63d0-fed1-43c2-824f-1d7c4f0589b7)


It's created Lambda, apigateway, CodeCommit repo

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/a37accee-ae96-4d81-9e8d-9d427c4e7c07)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/2d954cd6-3212-4f79-9060-980dbe4d19a7)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/8ba63fc3-f6b3-4b97-88cb-b007a1c0de1b)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/64e28479-9a9f-44cc-ac70-c04c556e3f15)


# Add logic to the web service

On the CloudShel CLI, you will perform all the commands.

Head inside the project folder, by listing the files first and then change the directory, run the below commands.

I change the statement in lambda function (index.py) 'Hello Word' to 'Hello from CodeStar'

I commit the change with git command 

$ git add -A

$ git commit -m "Change Hello Statement"

$ git push origin master

Now the changes are pushed. Let's go to CodeStar

The build phase fail

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/c7bc308d-f48f-4f9c-8591-8e60f2d94b2f)

Log execution build phase. AssertionError: 'Hello World' not found in '{"output": "Hello from CodeStar", "timestamp": "2024-02-17T09:27:43.559932"}'

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/bae965d2-da30-40ad-9223-089179f79736)

The reason, Unittest of CodeStar is looking for 'Hello word' in the output

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/f68f3101-4865-4723-a255-ef427d378655)

Fix the error. Change 'Hello Word' to 'Hello from CodeStar'

Let's change and puh again

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/d41267a4-c39d-4fcb-b02e-f87f86bd3f37)

Unittest succeed now. Let's see in the build console

As soon as run the git push command, changes are added to the CodeCommit repository, and the CodePipeline pipeline detects and changes and takes immediate action.

The source stage is where your code is getting updated.

In the build stage, the application’s required files are getting collected and the application is getting build.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/1c4001ca-645e-4431-8db2-39bae80937c2)

# changes are done in the pipeline

Navigate to CodeStar by clicking on the Services menu at the top, under the Developer Tools section.

Navigate to Projects from the left panel, and click on the project present. Switch to the pipeline tab and wait until all the stages show the status as succeeded.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/4f253c91-43b7-48b2-b72b-4fdfad1eadc6)

## The pipeline looking

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/4e85749d-bac2-4768-a3dd-06cf7f3750a6)

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/a1c70e18-6efb-496a-ae32-e0c49a07a1e4)


# Test the application an

Let's go to CodeStar dashbord

Navigate to Projects from the left panel, and click on the project present. Click on the View application to check the output.

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/082ba8b9-44bd-4b5c-84b8-4cd5b7f5a46d)


The output is the same as the change in index.py in cloud9 console

![image](https://github.com/felixdagnon/CodeStar-Deploying-and-Changing-Serverless-Patterns/assets/91665833/c2c5035d-be45-4d6a-9061-555a804526df)




















