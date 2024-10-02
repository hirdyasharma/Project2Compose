# Docker Compose Configuration for Jenkins
# CI/CD Pipeline for Node.js Application

## Project Overview
This project implements a Continuous Integration (CI) and Continuous Deployment (CD) pipeline for a Node.js web application using Jenkins and Docker. The pipeline automates the build, test, and deployment processes within a containerized environment, utilizing Docker-In-Docker (DinD) technology.

## Prerequisites
Before you begin, ensure you have the following:
- A Linux server running Ubuntu 20.04 (or similar).
- Docker and Docker Compose installed.
- A personal GitHub account.

## Project Structure
- **Project2Compose**: Repository for Docker Compose configuration.
- **aws-elastic-beanstalk-express-js-sample**: Forked repository containing the Node.js web application.

## Installation Instructions

### Step 1: Clone the Repositories
Clone the repositories to your local machine:

git clone https://github.com/hirdyasharma/aws-elastic-beanstalk-express-js-sample.git
git clone https://github.com/hirdyasharma/Project2Compose.git
Comments: Cloning the repositories gives you access to both the Node.js application and the Docker Compose configuration.

Step 2: Set Up Docker Compose
Navigate to the Project2Compose directory and run Docker Compose to start Jenkins and DinD:

bash
Copy code
cd Project2Compose  # Change to the Docker Compose directory
docker-compose up -d  # Start Jenkins and DinD containers in detached mode
Comments: This command launches Jenkins in a Docker container along with the Docker-In-Docker service, allowing Jenkins to run Docker commands.

Step 3: Access Jenkins
Open your web browser and navigate to Jenkins:

plaintext
Copy code
http://<your-server-ip>:8080  # Replace <your-server-ip> with your server's IP address
Comments: Access Jenkins through the web interface to set up your pipeline.

Step 4: Configure Jenkins Pipeline
Create a New Pipeline Project:

In Jenkins, click on "New Item."
Enter a name for your project (e.g., StudentID_Project2_pipeline) and select "Pipeline."
Click "OK."
Configure the Pipeline:

Scroll down to the "Pipeline" section.
Select "Pipeline script from SCM."
Choose "Git" as your SCM.
Enter the repository URL for your forked Node.js application:
plaintext
Copy code
https://github.com/hirdyasharma/aws-elastic-beanstalk-express-js-sample.git
Set the branch to main (or your default branch).
Click "Save."
Comments: This sets up Jenkins to use the Jenkinsfile from your Node.js application repository for the CI/CD pipeline.

Step 5: Run the Pipeline
Trigger the Pipeline:
In the Jenkins dashboard, click on your newly created project.
Click on "Build Now" to run the pipeline.
Monitor the Pipeline:
Click on the build number (e.g., #1) to see the build details.
Check the console output for logs and execution status.
Comments: This starts the CI/CD process, executing the steps defined in the Jenkinsfile.

Step 6: Review Pipeline Logs
After the pipeline runs, review the logs for any errors or important messages.
Take screenshots of the successful pipeline execution and logs for documentation.
Comments: Reviewing logs helps ensure that all steps executed successfully and helps identify any potential issues.

Conclusion
This project demonstrates how to implement a CI/CD pipeline for a Node.js application using Jenkins and Docker. The automated pipeline streamlines the development and deployment process, adhering to modern DevOps practices.

References
Jenkins Documentation: Jenkins Docs
Docker Documentation: Docker Docs
Snyk Documentation: Snyk Docs
Node.js Documentation: Node.js Docs
Docker-In-Docker Guide: Docker-In-Docker
Jenkins Pipeline Documentation: Jenkins Pipeline
GitHub Repository for Node.js Sample App: Node.js Sample App
