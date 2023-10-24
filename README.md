# serverless-express-aws-lambda
An express serverless lambda project configured with typescript deployed with AWS CDK

This stack deploys:
- CI/CD pipeline
- lambda function with serverless-express
- Error alarm with pipeline rollback functionality

### Tutorial
https://medium.com/itnext/building-a-ci-cd-pipeline-for-a-serverless-express-application-with-aws-cdk-1d3c842ea1ff

### Setup
#### Install deps
```
cd deployment
npm install
```

#### Setup configuration
https://github.com/devkit-io/serverless-express-aws-lambda/blob/main/deployment/bin/config.ts
```
export const configuration = {
  repoOwner: "__REPO_OWNER__",
  repoName: "__REPO_NAME__",
  codeBranch: "__CODE_BRANCH__",
  connectionArn: "__CONNECTION_ARN__",
  account: "__ACCOUNT__",
  region: "__REGION__",
}
```



#### AWS Credentials
Ensure your aws credentials are available in the environment
```
export AWS_ACCESS_KEY_ID=<value>
export AWS_SECRET_ACCESS_KEY_ID=<value>
```

### Synth
`cdk synth`

### Deploy
`cdk deploy`

### Automated deployment
To automate this deployment, visit https://dev-kit.io/deploy
