# Deployment of a high-availability web app using CloudFormation

This projects uses CloudFormation script to deploy a VPC with associated subnets and web application. There are two script, One for the the network infrastructure required to run the application:
`udagram-network-chuks.yml` and the other is for the server deployment: `udagram-servers-chuks.yml`

I used a Launch Configuration to deploy four webservers, 2 located in each of the private subnets. The launch configuration is used by an autoscaling group.

## Deployment Script

### To create the stack

To create the stack using CloudFormation, you run the following command

```
./create.sh <stack-name> <template-body>.yml <parameters>.json <aws-profile-name>
```

Example:

```
./create.sh chuksudagramproject2 udagram-network-chuks.yml udagram-network-params.json devOps-admin
```

### To update the stack

To update the stack using CloudFormation, you run the following command

```
./update.sh <stack-name> <template-body>.yml <parameters>.json <aws-profile-name>
```

Example:

```
./update.sh chuksudagramproject2 udagram-network-chuks.yml udagram-network-params.json devOps-admin
```
