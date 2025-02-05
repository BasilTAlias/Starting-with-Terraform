# Terraform AWS VPC Project

This project demonstrates the creation of a Virtual Private Cloud (VPC) on AWS using Terraform. The VPC includes a public subnet, a private subnet, an Internet Gateway, and route tables for proper network routing. The project is designed to be simple and easy to understand, making it a great starting point for learning Terraform and AWS networking.

---

## Project Overview

This Terraform project creates the following AWS resources:
- **VPC**: A Virtual Private Cloud with a specified CIDR block.
- **Public Subnet**: A subnet with a route to the Internet Gateway.
- **Private Subnet**: A subnet with no direct route to the Internet.
- **Internet Gateway**: Allows communication between the VPC and the Internet.
- **Route Tables**: Public and private route tables to manage traffic routing.

---

## Prerequisites

Before using this project, ensure you have the following:
1. **AWS Account**: You need an AWS account with the necessary permissions to create VPCs, subnets, and other resources.
2. **AWS CLI**: Install and configure the AWS CLI with your credentials.

##  Repository Structure

The repository contains the following files:

- **main.tf**: Defines the AWS resources (VPC, subnets, Internet Gateway, route tables, etc.).

- **variables.tf**: Contains variables for the AWS region, VPC CIDR block, subnet CIDR blocks, and availability zone.

---
$~$

## **Terraform Variables**

| Variable | Description | Default |
|----------|-------------|----------|
| `aws_region` | AWS region to deploy resources | `us-east-1` |
| `vpc_cidr` | CIDR block for the VPC | `10.0.0.0/16` |
| `public_subnet_cidr` | CIDR block for public subnet | `10.0.1.0/24` |
| `private_subnet_cidr` | CIDR block for private subnet | `10.0.2.0/24` |
| `availability_zone` | Availability zone for subnets | `us-east-1a` |
  
$~$


## **Terraform Commands**

### **1. Initialize Terraform**
```sh
terraform init
```
This command downloads necessary provider plugins and sets up the backend configuration.

### **2. Validate Configuration**
```sh
terraform validate
```
Checks for syntax errors in your Terraform files.

### **3. Plan Deployment**
```sh
terraform plan
```
Generates an execution plan, showing the resources that will be created.

### **4. Apply Configuration**
```sh
terraform apply
```
Deploys the infrastructure. You will be prompted for confirmation (`yes`).

### **5. View Created Resources**
```sh
terraform show
```
Displays the current Terraform state and resources created.

### **6. Destroy Infrastructure**
```sh
terraform destroy
```
Deletes all the resources created by Terraform.

---
$~$


## Screenshots

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/1.png)

Current VPC details

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/2.png)

Set up and configure the AWS CLI using 

$~$
```sh
aws configure
```
The AWS configure command is used to set up and configure the AWS CLI (Command Line Interface) with your AWS credentials and default settings.

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/3.png)

Retrieve details about the AWS account

$~$
```sh
aws sts get-caller-identity
```
The AWS sts get-caller-identity command is used to retrieve details about the AWS account and IAM user or role associated with the current AWS credentials. It is a simple way to verify that your AWS CLI is configured correctly and that you have valid credentials.

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/4.png)

Terraform version details

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/5.png)

Configured the core files ( main.tf & variables.tf)

These files are the core of your Terraform configuration. They define the infrastructure resources and the variables used to customize the deployment.

1. main.tf
Purpose: Contains the main configuration for your AWS resources (e.g., VPC, subnets, Internet Gateway, etc.).

2. variables.tf
Purpose: Defines variables used in the main.tf file, making the configuration reusable and customizable.

$~$
![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/6.png)

Initializing terraform

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/7.png)

Plan Deployment

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/8.png)

Generates an execution plan, showing the resources that will be created

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/9.png)

Apply configuration

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/10.png)

Typing yes when prompted to confirm the creation of resources

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/11.png)

Verify Resources: -> Newly created VPC details

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/12.png)

Newly created VPC resource map details

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/13.png)

$~$
![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/14.png)

Destroys all the resources created by the Terraform configuration

$~$

![Alt text of the image](https://github.com/BasilTAlias/Starting-with-Terraform/blob/main/images/15.png)

Current VPC details; VPC destroyed successfully

$~$

## Conclusion

This Terraform project provides a simple yet powerful example of how to create and manage AWS VPC infrastructure using Infrastructure as Code (IaC). By leveraging Terraform, you can automate the provisioning of cloud resources, ensure consistency across environments, and easily manage changes through version control.

The project highlights key AWS networking concepts, such as VPCs, subnets, route tables, and Internet Gateways, while demonstrating best practices for structuring Terraform configurations. Whether you're new to Terraform or looking to expand your AWS knowledge, this project serves as a solid foundation for building more complex infrastructure.
