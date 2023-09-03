<h1 align="center">CloudWeaver</h1>

<!-- Project Description -->
<p align="center">A secure and scalable VPC foundation for AWS resources</p>


<!-- Table of Contents -->
## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [Customization](#customization)
- [Deployment](#deployment)
- [Documentation](#documentation)


<!-- Project Overview -->
## Project Overview

The goal of this project is to create a secure and scalable Virtual Private Cloud (VPC) that serves as the foundation for deploying various AWS resources. This README provides an overview of the project's components, deployment instructions, and customization options.

## Getting Started

#### Prerequisites

Ensure that you have the following prerequisites in place:
- AWS CLI configured with necessary credentials (see [AWS CLI Configuration](#aws-cli-configuration)).
- AWS CloudFormation knowledge and access.

#### AWS CLI Configuration

If you haven't already, configure your AWS CLI with the necessary credentials, region, and output format by editing the `~/.aws/config` file. You can use the `[default]` profile or create a named profile.

#### Customization
Edit the parameters.json file to customize the VPC deployment. Specify parameters such as VPC CIDR blocks, subnet CIDR blocks, and resource names.

#### Deployment
Use the AWS CLI to create the CloudFormation stack and deploy the VPC. See Deployment for details.


## Customization
You can customize the VPC deployment by editing the parameters.json file. Here are some of the parameters you can customize:

#### VPC CIDR Block:
The IPv4 CIDR block for the VPC.

#### Subnet CIDR Blocks:
The CIDR blocks for public and private subnets.

#### Resource Names:
Names for various AWS resources, such as subnets, security groups, and route tables.

#### Other Configuration Options:
Depending on your project's complexity, you can customize additional parameters and resources in the CloudFormation template.



## Deployment
To deploy the VPC and associated resources, follow these steps:

1- Open a terminal.

2- Navigate to the project directory containing the CloudFormation template [(vpc.yaml)](vpc.yaml). and the parameters file [(parameters.json)](parameters.json)..

3- Run the following AWS CLI command to create the CloudFormation stack:

        aws cloudformation create-stack --stack-name MyVPCStack --template-body file://vpc.yaml --parameters file://parameters.json
        
4- Monitor the stack creation progress using the AWS CloudFormation console or the AWS CLI.

Once the stack is created successfully, you can access and use the VPC and associated resources as needed.

## Documentation
For detailed documentation on the project, please refer to the [documentation directory](docs/).

<h1 align="center">THANK YOU! </h1>


