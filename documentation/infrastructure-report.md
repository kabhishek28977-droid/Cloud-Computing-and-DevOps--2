# AWS Infrastructure Report

## 1. Project Overview

This project demonstrates the setup of a basic AWS cloud infrastructure using Amazon VPC and related AWS services.

## 2. AWS Services Used

- Amazon VPC
- Subnets
- Internet Gateway
- Route Tables
- Security Groups
- Amazon EC2
- Amazon S3
- Amazon CloudWatch

## 3. VPC Configuration

A VPC was created with the CIDR block:

`10.0.0.0/16`

DNS resolution and DNS hostnames were enabled for the VPC.

## 4. Subnet Configuration

Public and private subnets were created inside the VPC.

The public subnet is associated with a route table that provides internet access through the Internet Gateway.

The private subnet is intended for resources that do not require direct internet access.

## 5. Internet Gateway

An Internet Gateway was created and attached to the VPC.

The public route table contains:

`10.0.0.0/16 → local`

`0.0.0.0/0 → Internet Gateway`

This allows resources in the public subnet to communicate with the internet.

## 6. Route Table

The route table was configured with a local VPC route and a default route through the Internet Gateway.

## 7. Security Group

A security group was configured to control inbound and outbound traffic for the EC2 instance.

## 8. EC2 Instance

An EC2 instance using the `t3.micro` instance type was configured.

The instance was used for testing the cloud infrastructure and running an Nginx web server.

## 9. Nginx

Nginx was installed and configured on the EC2 instance to provide a web server.

## 10. Amazon S3

An S3 bucket was created for cloud storage.

## 11. Amazon CloudWatch

CloudWatch was used for monitoring AWS resources and infrastructure metrics.

## 12. Architecture Diagram

The AWS architecture diagram is stored in the `architecture/` directory.

## 13. Screenshots

Screenshots documenting the AWS infrastructure are stored in the `screenshots/` directory.

The screenshots include:

- VPC
- Subnets
- Public Subnet
- Private Subnet
- Internet Gateway
- Route Table
- Security Group
- EC2
- S3
- CloudWatch
- Nginx

## 14. Conclusion

The project demonstrates the basic implementation of AWS networking, compute, storage, monitoring, and web-server infrastructure.

All major configuration steps are documented with screenshots and supporting project files.
