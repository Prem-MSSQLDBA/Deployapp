## Capstone Project
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Prem-MSSQLDBA/Deployapp/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Prem-MSSQLDBA/Deployapp/tree/main)

## Project Overview
This Capstone project will utilize CI/CD and cloud services learned during the Udacity - AWS Cloud DevOps Engineer nanodegree.

Plan what your pipeline will look like.
Decide which options you will include in your Continuous Integration phase. Use either Circle CI or Jenkins.
Pick a deployment type - either rolling deployment or blue/green deployment.
For the Docker application you can either use an application which you come up with, or use an open-source application pulled from the Internet, or if you have no idea, you can use an Nginx “Hello World, my name is (student name)” application.

## Steps
- Create Dockerfile
- Circleci pipeline runs lint tests on Dockerfile to ensure Dockerfile is suited to be uploaded to repository
- Dockerfile is built and then uploaded to Docker repository automatically by CircleCi using  scripts.
- EKS cluster is deployed automatically by CircleCI using AWS Cli - status of creation of EKS cluster can be viewed in Cloudformation of AWS.
- Docker application which was uploaded to Docker repository is deployed in EKS cluster by using Kubernetes command line.

## Requirements
Configure the following variables in your CircleCi project:
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- AWS_DEFAULT_REGION
- DOCKER_LOGIN
- DOCKER_PASSWORD
