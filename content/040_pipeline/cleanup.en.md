+++
title = "Cleanup"
weight = 49
+++

#### Delete the stacks for each environment created for our application

```sh
aws cloudformation delete-stack --stack-name serverless-service-Dev
aws cloudformation delete-stack --stack-name serverless-service-Prod
```

#### Delete the code repository

```sh
aws codecommit delete-repository --repository-name serverless-repo
```

#### Delete the build projects

```sh
aws codebuild delete-project --name serverless-build-project
aws codebuild delete-project --name serverless-test-project
```

#### Delete the pipeline

```sh
aws codepipeline delete-pipeline --name serverless-pipeline
```

#### Empty and delete the S3 bucket for build artifacts

```sh
aws s3 rm s3://aws-serverless-catalog-wksp-build-<FIRSTNAME-LASTNAME> --recursive
aws s3 rb s3://aws-serverless-catalog-wksp-build-<FIRSTNAME-LASTNAME> --force
```

#### Delete the IAM Roles

```sh
aws iam delete-role --name 
```
