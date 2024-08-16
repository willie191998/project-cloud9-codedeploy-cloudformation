### NextWork Web Deployment Project
This repository contains the necessary scripts and configuration files for deploying the NextWork web application using AWS services. The deployment process is automated through AWS CodeDeploy, with supporting resources such as S3, EC2, IAM, and CloudFormation.

## Resouirces Used
Cloud9
Cloudformation
Codebuild
Codedeploy
GitHub
S3

## Project Structure

# scripts/

**install_dependencies.sh**: Installs necessary dependencies for the application.
**start_server.sh**: Starts the Tomcat and Apache services.
**stop_server.sh**: Stops the Tomcat and Apache services.
**buildspec.yml**: Defines the build commands for AWS CodeBuild, including compiling and packaging the application.

**appspec.yml**: Configures the deployment settings, specifying the location of scripts and where to deploy the application.

## Deployment Process
**Create IAM Role**: A role with the necessary permissions to interact with AWS CodeDeploy and other services.
**Configure CodeDeploy**: Set up an application and deployment group in CodeDeploy, linking it to your EC2 instances.
**Deploy Application**: Use CodeDeploy to automate the deployment of your application, including uploading the build artifacts to S3 and deploying them to your EC2 instances.

## Usage

Clone the repository to your AWS Cloud9 environment.
Edit the buildspec.yml and appspec.yml files with your specific project details.
Commit and push your changes to AWS CodeCommit.
Trigger a build in CodeBuild and monitor the deployment through CodeDeploy.

## Clean Up
Ensure that you delete all resources created during this process to avoid unnecessary charges.
