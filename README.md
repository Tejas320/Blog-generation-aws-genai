# Blog generation using AWS Lambda and AWS BedRock

## Overview
This project leverages AWS Lambda and AWS Bedrock to create a serverless blog generation pipeline. The system automates content creation using advanced AI models hosted on AWS Bedrock, triggered by AWS Lambda functions. It's designed to efficiently generate high-quality blog content without the need for managing servers or infrastructure.

## Architecture
The project follows a serverless architecture:
![image](https://github.com/user-attachments/assets/2f4dc5fb-f201-4ae6-8a05-ec59082c8328)

AWS Lambda: Handles the orchestration of the blog generation process, invoking AI models, and managing data flow.

AWS Bedrock: Provides the AI models used for generating blog content, including text generation and content refinement.

S3: Stores the generated blog content and related assets.

API Gateway: (Optional) Exposes a RESTful API to trigger the blog generation process.

## Features
Serverless: Fully managed by AWS, with no server maintenance required.

Scalable: Automatically scales to handle any number of blog generation requests.

Customizable: Easily adjust the AI models and parameters used for content creation.

Secure: Leverages AWS IAM roles and policies for secure access and operation.

## Prerequisites
Before you begin, ensure you have the following:

An AWS account with permissions to create and manage Lambda functions, API Gateway, S3, and access to AWS Bedrock.

AWS CLI configured with your credentials.

Basic knowledge of Python programming language.

## Important steps

1. Created a new function `awsappbedrock` in AWS Lambda with Python 3.12 as runtime.
2. Created a new virtual environment (venv) in VS Code with Python version 3.12 and activated it.
3. Created a new file `app.py` writing the lambda function code using Llama 3 8B Instruct model.
   ### Note: Please refer `app.py` file provided above for detailed code.
4. Copy paste the code from VS Code to  Code Source in AWS Lambda and deploy it.
5. Whenever we open a lambda function, by default it uses an older version of `boto3` installled. To resolve this, we need to update packages.
6. Created a new folder in VS Code with `boto3` library installed in it. Run this command in the terminal.
   ```bash
   pip install boto3 -t python/
   ```
7. Once this folder is created, make a zip file of this folder.
   ### Note: 
