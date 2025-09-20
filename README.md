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

# STEPS BY STEPS PROCESS 

### 1. Launched 3 amazon linux 2 and 2 ubuntu server:

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/652c366e-9281-4c62-ab97-9560917463e8)


### 2. Installed ansible on linux-ansible-controller:

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/b44759ac-f49a-4102-acee-deaae6d83818)


### 3. Verified ansible is installed in linux-ansible-controller. And generated ssh key-pair. Copied the public key to all 4 nodes:

<img width="512" alt="image" src="https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/088d1bbd-a60b-441e-9b36-99c90b0a2390">


### 4. Updated “hosts” file in ansible-controller.

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/ae396a32-ee5a-4d9a-af68-18d0a6fb98ff)


### 5. Test the connectivity in-between the controller and nodes:

<img width="590" alt="image" src="https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/dffc2ab1-b43b-4a9e-bb38-ba771cc1cbd0">

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/a0f79a1a-2dd3-410c-bdde-452a0f8c9c46)


### 6. Run ansible-hw-playbook.yml file

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/e7502d8e-7abf-4fb0-b97c-775c844cd65d)

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/2557550e-851e-4ef5-accf-98254a3a55b4)


### 7. Connect to linux-node1 i.e. “ansible-linux-node1” and verify that index.html file is written in /var/www/html

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/a0ab4ddc-f45f-4797-b57e-50ded432d027)


### 8. Connect to ubuntu-node1 i.e. “ansible-node1” and verify that index.html file is written in /var/www/html

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/a73aef8d-0195-45e5-b497-4cde2b51104b)


### 9. Verify GIT is installed in both linux and ubuntu nodes:
![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/8c53e5b4-d676-4d7e-bee9-9435f725447c)

![image](https://github.com/Fokoue22/ANSIBLE-Project-on-AWS/assets/117523566/390358c6-d5c5-4ec5-9521-8346ec8e6aa7)












