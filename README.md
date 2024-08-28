
# AWS DevOps CI/CD Pipeline Project

Overview

This project demonstrates a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline using AWS services. It automates the process of building, testing, scanning, and deploying a Docker image to an Amazon EC2 instance.

Architecture

![image](https://github.com/user-attachments/assets/7ce95ac2-7186-449a-9adc-14fab4da489b)

Workflow:

1. User Commit: The user commits code to AWS CodeCommit.
2. CodePipeline: Triggers automatically on code changes in the repository.
3. CodeBuild:
Check out the code.
Executes build and unit tests.
Scans the code for vulnerabilities.
Builds the Docker image.
Scans the Docker image.
Pushes the Docker image to a container registry (e.g., Amazon ECR).
4. CodeDeploy: Deploys the Docker image to an Amazon EC2 instance.
 
Tools Used

👉 AWS CodeCommit: Stores the source code and version control.
👉 AWS CodePipeline: Orchestrates the CI/CD workflow.
👉 AWS CodeBuild: Executes build, unit tests, code scan, image build, and image scan.
👉 AWS CodeDeploy: Deploys the built image to the target EC2 instance.
👉 Amazon EC2: Hosts the application after deployment.

Detailed Pipeline Breakdown

1. Checkout: Pulls the latest code from CodeCommit.
2. Build & UT: Runs build steps and unit tests using CodeBuild.
3. Code Scan: Performs static code analysis for security and code quality.
4. Image Build: Constructs a Docker image of the application.
5. Image Scan: Checks for vulnerabilities in the built Docker image.
6. Image Push: Pushes the final image to Amazon Elastic Container Registry (ECR).
7. Deployment: CodeDeploy picks the image and deploys it to the Amazon EC2 instance.
   
Conclusion

This AWS DevOps pipeline automates the entire process of building, testing, scanning, and deploying your application, ensuring quicker releases and improved software quality.


