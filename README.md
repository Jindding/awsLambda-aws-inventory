# AWS Resource List Export (AWS Inventory)

## Table of Contents
- [Overview](#overview)
- [Purpose](#purpose)
- [Configuration](#configuration)
  - [Prerequisites](#prerequisites)
  - [Configuration Steps](#configuration-steps)
- [Available Export Resources](#available-export-resources)
## Overview
This project provides an AWS Lambda function that retrieves information about your AWS resources, including EC2 instances, S3 buckets, ALBs, Elasticache clusters, VPCs, subnets, IAM accounts, and Lambda functions. The collected data is then exported to an Excel file and uploaded to an S3 bucket. This function allows you to maintain a record of your AWS resources for documentation and auditing purposes.

## Purpose
The purpose of this AWS Lambda function is to automate the generation of an AWS resource inventory for your AWS account. It fetches critical information about various resource types and compiles it into an Excel spreadsheet for easy reference and record-keeping.

## Configuration
Before you can use this Lambda function, you need to configure it with your AWS credentials and specify the parameters for the function. Here's what you need to do:

### Prerequisites
- You should have an AWS account and access to the AWS Management Console.
- Ensure that you have the necessary IAM permissions for accessing the AWS resources you want to include in the inventory.

### Configuration Steps
1. **Region**: Set the `region` variable to your desired AWS region.

2. **S3 Bucket Configuration**: Specify the S3 bucket name and key where you want to store the Excel file. Modify the `s3_bucket_name` and `s3_key` variables accordingly.

## Available Export Resources
| Resource                    | Yes?                                           |
|----------------------------|-------------------------------------------------------|
| EC2 Instance               | :white_check_mark: |
| Application Load Balancer   | :white_check_mark: |
| S3 Bucket                  | :white_check_mark: |
| Elasticache Cluster        | :white_check_mark: |
| VPC                        | :white_check_mark: |
| Subnet                     | :white_check_mark: |
| IAM Account                | :white_check_mark: |
| Lambda Function            | :white_check_mark: |
