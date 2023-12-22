# AWS Lambda Hello World with Dockerized Deployment

This repository contains a simple "Hello World" program written in Python for AWS Lambda. Additionally, it includes a Dockerfile to containerize the pythom program, and the deployment process is automated through a Jenkins CI/CD pipeline. The Docker image is pushed to AWS ECR (Elastic Container Registry), and an AWS Lambda function is created using the ECR image.

## Prerequisites

Before you proceed, make sure you have the following installed:

- Docker: [Docker Installation](https://docs.docker.com/get-docker/)
- AWS CLI: [AWS CLI Installation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
- Jenkins: [Jenkins Installation](https://www.jenkins.io/doc/book/installing/)
- AWS Lambda Role: Create an AWS Lambda Role with read-only permission to AWS ECR.

Ensure that your AWS CLI is configured with the necessary credentials and permissions.

## Project Structure

- ├── hello_world_lambda.py # Hello World AWS Lambda function code
- ├── Dockerfile # Dockerfile for building the Lambda function container
- ├── Jenkinsfile # Jenkins pipeline script for CI/CD
- └── README.md # Project documentation

## Getting Started

1. **Clone this repository:**

   ```bash
   git clone https://github.com/yogendra-kokamkar/docker-ecr-lambda.git
   cd docker-ecr-lambda

2. **Customize the Lambda function code:**

    Modify the hello-world-lambda.py file according to your requirements.

3. **Update Jenkinfile:**

    Modify the jenkinsfile and replace the placeholders like AWS Region, AWS Account ID, Git URL, etc as per your requirements.

## Building and Deploying with Jenkins
1. **Set up a Jenkins job:**

    Create a new Jenkins job.
    Configure the job to use the provided Jenkinsfile.

2. **Trigger the Jenkins job:**

    Push changes to your repository or manually trigger the Jenkins job.

3. **Jenkins CI/CD Pipeline:**  

    The pipeline will build the Docker image, push it to AWS ECR, and create/update the Lambda function.

## Notes
Ensure that your AWS credentials are securely configured in Jenkins to allow it to interact with AWS services.
Customize the AWS region and other parameters in the Jenkinsfile as needed.
Feel free to explore and extend this project to meet your specific requirements. If you encounter any issues or have suggestions for improvements, please open an issue in this repository.