# AWS Resource List Export (AWS Inventory)

## Table of Contents
- [Overview](#overview)
- [Purpose](#purpose)
- [Configuration](#configuration)
  - [Prerequisites](#prerequisites)
  - [Configuration Steps](#configuration-steps)

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
1. **Access Key and Secret Key**: Replace the placeholders in the code with your AWS Access Key and Secret Key. It's recommended to use IAM roles and avoid hardcoding credentials for better security.

2. **Region**: Set the `region` variable to your desired AWS region.

3. **S3 Bucket Configuration**: Specify the S3 bucket name and key where you want to store the Excel file. Modify the `s3_bucket_name` and `s3_key` variables accordingly.
