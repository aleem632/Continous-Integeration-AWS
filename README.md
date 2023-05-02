# Continous-Integeration-AWS
- AWS CodeCommit
- AWS Codedeploy
- AWS Codebuild
- AWS CodeArtifact
- AWS CodePipeline for Integeration.

### AWS SERVICES

![CI-AWS](https://github.com/aleem632/Continous-Integeration-AWS/blob/0f9f8fd7b0231d0b6a0b0766abc0e63dbca77803/Diagram/CI-AWS.png)


### PROBLEMS
- CI Server Maintenance
- Operational overhead to maintain server like Jenkins, Nexus, Sonar,Git etc
### Solution
- Cloud services for Continous Integeration to remove Ops overhead

### BENEFITS
- Short MTTR
- Agile
- No human intervention
- Fault isolation 
- No Ops

### FLOW OF EXECUTION

![AWS](https://github.com/aleem632/Continous-Integeration-AWS/blob/70bb7038924e0d5da531620b0bb0310c9e8fbe48/Diagram/Continous-Integeration.png)

- Login to AWS Account
##### Code commit 
    - Create codecommit repo
    - create iam user with codecommit policy
    - Generate ssh keys locally
    - Exchange keys with IAM user
    - Put source code from github to repo to codecommit repository         and push
 ### AWS CODE ARTIFACT
 - Create AN IAM user with code artifact access
 - Install AWS CLI, Configure
 - Export auth token
 - update setting.xml file in source code
 - update pom.xml file with repo detail
 ### SONAR CLOUD
 - Create sonar cloud account
 - Generate token
 - Create SSM parameters with sonar details
 - Create build project
 - Update codebuild role to access SSMparameterstore
 ### CREATE NOTICATION WITH SNS OR SLACK
 ### BUILD PROJECT
 - Update pom.xml with artifact version with timestamp
 - Create variables with SSM
 - Create build project
 - update codebuild role to access SSMparameter store
 ### CREATE PIPELINE
 - Codecommit 
 - Testcode 
 - Build 
 - Deploy to s3 bucket
 ### TEST PIPELINE
 
 
 
 
