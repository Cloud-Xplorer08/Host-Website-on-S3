# Create S3 Bucket Using CLI

## Overview
In this lab, we practice using AWS Command Line Interface (AWS CLI) commands from an Amazon Elastic Compute Cloud (Amazon EC2) instance to:

- Create an Amazon Simple Storage Service (Amazon S3) bucket.

- Create a new AWS Identity and Access Management (IAM) user that has full access to the Amazon S3 service.

- Upload files to Amazon S3 to host a simple website for the Café & Bakery.

![architecture](https://github.com/Cloud-Xplorer08/Host-Website-on-S3/assets/71820244/d0da764e-2615-486a-ab67-27ffa4af043e)

## Task 1: Use SSH to connect to an Amazon Linux EC2 instance
In this task, we will log into an existing EC2 instance.Connect EC2 instance with Puttty

![connect with ec2](https://github.com/Cloud-Xplorer08/Host-Website-on-S3/assets/71820244/5254e15c-9b90-47f8-91c0-cdfefd65bcd3)

Use public-ip and PPK file to connect with putty

## Task 2: Configure the AWS CLI

![aws configure](https://github.com/Cloud-Xplorer08/Host-Website-on-S3/assets/71820244/bd93ecac-75c0-4c01-ade6-f35fffedb066)

## Task 3: Create an S3 bucket using the AWS CLI
The s3api command creates a new S3 bucket with the AWS credentials in this lab. By default, the S3 bucket is created in the us-east-1 Region.
When you create a new S3 bucket, the bucket must have a unique name, such as the combination of your first initial, last name, and three random numbers.

![bucket created](https://github.com/Cloud-Xplorer08/Host-Website-on-S3/assets/71820244/3cd01ccf-e744-4b62-bb7c-f988a2983e43)

#### aws s3api create-bucket --bucket new08buckt  --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2
new bucket created new08buckt

## Task 4: Create a new IAM user that has full access to Amazon S3
The AWS CLI command: aws iam create-user creates a new IAM user for your AWS account. The option --user-name is used to create the name of the user and must be unique within the account. 

![user and password created](https://github.com/Cloud-Xplorer08/Host-Website-on-S3/assets/71820244/c3e41927-2eb6-4f17-8f39-cc8ca981942b)
