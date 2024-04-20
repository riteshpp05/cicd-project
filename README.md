CI/CD Pipeline for Web Application
This repository contains a simple CI/CD pipeline for a web application using GitHub Actions. The pipeline automates testing and deployment to DockerHub.

Application Overview
The web application is a basic Flask app that returns "Hello World!" when accessed.

CI/CD Workflow
Workflow Overview
The CI/CD pipeline consists of two main jobs:

Build: Builds the Docker image of the application and pushes it to DockerHub.
Test: Runs unit tests using pytest.
Workflow Details
Build Job:
Runs on: Ubuntu latest
Steps:
Checkout code from the repository.
Login to DockerHub using the provided credentials.
Build, tag, and push the Docker image to DockerHub.
Test Job:
Runs on: Ubuntu latest
Steps:
Checkout code from the repository.
Set up Python environment.
Install dependencies.
Run unit tests using pytest.
Trigger
The workflow is triggered on every push to the main branch.

How to Run the Application Locally
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/your-repository.git
Navigate to the project directory:
bash
Copy code
cd your-repository
Build the Docker image:
bash
Copy code
docker build -t my-image .
Run the Docker container:
bash
Copy code
docker run -p 8080:8080 my-image
Access the application in your web browser at http://localhost:8080.
#Notes
Replace your-username and your-repository with your GitHub username and repository name.
Ensure that Docker is installed and running on your system to build and run the Docker image.
