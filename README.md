# Enterprise AWS VPC Project

## Objective

Design and deploy a secure enterprise-grade VPC using AWS networking services.

## Technologies

- AWS VPC
- EC2
- Internet Gateway
- NAT Gateway
- Route Tables
- S3 Gateway Endpoint
- IAM

## Architecture

![Enterprise VPC Diagram](aws-screenshot/enterprise-vpc.png)

## Features

- Public subnet
- Private subnet
- Internet connectivity
- Outbound-only internet for private resources
- Private S3 access via endpoint
- Bastion host administration

## Testing

### NAT Gateway Validation

Private EC2 successfully downloaded packages through NAT Gateway.

### S3 Endpoint Validation

Private EC2 uploaded objects to S3 without internet access.


  📑 **Project Overview**
- [Custom VPC](#custom-vpc)
- [Public Subnet](#public-subnet)
- [Private Subnet](#private-subnet)
- [Internet Gateway](#internet-gateway)
- [NAT Gateway](#nat-gateway)
- [Route Tables](#route-tables)
- [Security Groups](#security-groups)
- [EC2-Instance](#ec2-instance)
- [S3 Gateway Endpoint](#s3-gateway-endpoint)


## Custom VPC
We are going to create a VPC called MyVPC. Make sure your browser is logged in to the AWS Management Console.
## Step 1: Create a VPC

1. Go to the **VPC** service in the AWS Management Console.
2. Click **Your VPCs** → **Create VPC**.
3. Choose the **VPC only** option.
4. Configure the VPC with the following settings:
   - **Name:** `MyVPC`
   - **IPv4 CIDR block:** `10.0.0.0/16` *(enough for many subnets)*
   - **IPv6 CIDR block:** `No IPv6`
   - **Tenancy:** `Default`
5. Click **Create VPC**.

✅ You now have a VPC.
