# CI/CD Pipeline with Python, Flask, and Docker

This project demonstrates the creation of a Continuous Integration and Continuous Deployment (CI/CD) pipeline for a simple Python Flask application. The pipeline automates the building, testing, and deployment of the Flask app using Docker and GitHub Actions.

## Project Overview

This repository includes a complete CI/CD workflow that:
- Uses **GitHub Actions** for automation.
- Builds a Docker image for a simple **Flask** application.
- Runs automated tests and linting on the application.
- Deploys the application using Docker.

## Key Components

- **GitHub Actions**: Automates the process of building, testing, and deploying the application.
- **Docker**: Containerizes the Python Flask application.
- **Flask**: A simple Python web application.

## Project Structure

- **.github/workflows/ci.yml**: The GitHub Actions configuration file that defines the CI/CD pipeline.
- **Dockerfile**: The configuration for creating a Docker image of the Flask application.
- **app.py**: The main Python Flask application.
- **requirements.txt**: A file listing the required Python packages for the application.

## Setup and Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/ci-cd-python-pipeline.git
   cd ci-cd-python-pipeline

2. Build the Docker image locally (optional):
   ```bash
   docker build -t your-docker-image-name .

3. Push the Docker image to Docker Hub:
   ```bash
   docker push your-docker-image-name

4. Run the Docker container:
   ```bash
   docker run -p 5000:5000 your-docker-image-name

5. Open your browser and go to http://localhost:5000 to see the application running.

 
## How It Works

The CI/CD pipeline is triggered whenever changes are pushed to the main branch.

**GitHub Actions**:
- Checkout the code.
- Set up the Python environment and install dependencies.
- Run tests with `unittest`.
- Build and push the Docker image to Docker Hub.
- Deploy the Docker container to your local machine or any environment.

## CI/CD Workflow

The CI/CD pipeline is configured in `.github/workflows/ci.yml`. It includes the following steps:
- **Checkout**: Fetches the code from the repository.
- **Set up Python**: Installs the required version of Python and dependencies from `requirements.txt`.
- **Docker Build**: Builds the Docker image.
- **Test Execution**: Runs unit tests to ensure code correctness.
- **Docker Push**: Pushes the Docker image to Docker Hub.
- **Docker Run**: Deploys the application using Docker.

## License

MIT License - see LICENSE for details.

Feel free to open issues or submit pull requests if you would like to contribute to this project.

## Future Enhancements

- Implement monitoring and logging for the deployed application.
- Integrate more advanced security practices like image scanning.
- Add automated deployment to different environments (e.g., staging, production).


  

