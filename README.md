# Medusa Project

This repository is configured to automate the process of building and pushing a Docker image to Amazon Elastic Container Registry (ECR) using GitHub Actions. The workflow is triggered when changes are pushed to the `medusa` branch.

## Overview

The project contains a Docker setup for the Medusa Store. GitHub Actions is used to automate the process of building the Docker image and pushing it to AWS ECR.

### Features

- **Automated Docker Builds**: On every push to the `medusa` branch, the workflow builds the Docker image from the `my-medusa-store` folder.
- **Push to Amazon ECR**: The built Docker image is automatically pushed to a specified ECR repository in AWS.
- **GitHub Secrets**: AWS credentials and configuration are securely managed via GitHub Secrets.

## Prerequisites

Before using this repository, ensure that the following requirements are met:

1. **AWS Account**: An AWS account with access to Elastic Container Registry (ECR).
2. **AWS CLI Configuration**: The AWS CLI should be installed and configured with the necessary permissions to push Docker images to ECR.
3. **GitHub Secrets**: The following secrets must be set up in the GitHub repository:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION`
   - `ECR_REPOSITORY`

## Setup

1. **Create an ECR Repository**: Log in to your AWS account, create an ECR repository, and note the repository URI.
2. **Add GitHub Secrets**: In the GitHub repository settings, add the AWS credentials and ECR repository name as secrets.
3. **GitHub Actions Workflow**: A pre-configured GitHub Actions workflow is set up in `.github/workflows/docker-build.yml` to automate the Docker build and push process.

## Usage

- **Branch**: The workflow is triggered by any push to the `medusa` branch.
- **Manual Trigger**: You can also manually trigger the workflow from the **Actions** tab in the GitHub repository.

## AWS Elastic Container Registry (ECR)

After the workflow completes, the Docker image will be available in your specified ECR repository. You can verify this by logging into your AWS account and checking the ECR repository for the latest image.

## Contributing

Feel free to fork this repository and submit pull requests. Contributions are welcome!


