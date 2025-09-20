# cloudformation-april2025
Deploying a Flask Email Database on AWS with CloudFormation: A Step-by-Step Guide

## PROJECT DESCRIPTION
![Alt text](images/setup.gif)

If you’re looking to deploy a web application with a database on AWS without breaking a sweat, this guide is for you. We’ll walk through automating the deployment of a simple Flask-based email database application using AWS CloudFormation. This app lets users add and retrieve email addresses, with the backend powered by AWS RDS and secrets stored securely in AWS Secrets Manager. Let’s dive in with a clear, hands-on approach to get this up and running.

### Demo
![Alt text](images/setup2.gif)

### 1-  Deploy Our Network Template  
* we will add SSH to our Security Group in the template that was provided
![Alt text](images/step1.png)

```
aws cloudformation create-stack --stack-name my-stack --template-body file://CFN-Template.yaml --region <your-region> --capabilities CAPABILITY_IAM
```












