
# Devops Maya

This project involves developing a common Autodesk Maya environment for an animation company.
A CI/CD and container orchestration solution should also be considered.
## Project Goals

1. Develop a Common Maya Environment: Create a standardized Maya environment that can be shared across the animation company. This includes setting up a base Docker image with Autodesk Maya and the required dependencies.

2. CI/CD Implementation: Set up a CI/CD pipeline using Jenkins to automate the build, test, and deployment processes for Maya projects. This involves integrating version control, building Docker images, running tests, and deploying the applications to different environments.

3. Container Orchestration with Kubernetes: Utilize Kubernetes to manage and orchestrate the deployment of Maya applications across multiple containers. This provides scalability, fault tolerance, and efficient resource utilization for Maya rendering and processing.
## Approach

1. Dockerizing Maya:
    - Create a Docker image that includes Autodesk Maya, the necessary libraries, and tools.
    - Set up the image to support rendering and other Maya-specific tasks.

2. CI/CD Pipeline with Jenkins:
    - Configure Jenkins to monitor version control repositories for changes.
    - Set up automated builds triggered by code changes.
    - Perform testing, including running automated tests for Maya projects.
    - Implement deployment pipelines to different environments (development, staging, production).

3. Kubernetes Orchestration:
    - Deploy Kubernetes clusters to manage Maya applications.
    - Utilize Kubernetes resources such as Deployments, Services, and Pods for managing containers.
    - Configure resource limits, scaling policies, and health checks for optimal performance.
## Benefits

- **Consistent Maya Environment**: Dockerizing Maya ensures consistent environments across development, testing, and production stages.

- **Automated CI/CD Processes**: Jenkins automates building, testing, and deployment processes, reducing manual effort and improving productivity.

- **Scalability and Fault Tolerance**: Kubernetes enables scaling Maya applications based on demand and provides fault tolerance for reliable and efficient processing.

- **Standardization and Collaboration**: A common Maya environment allows teams to collaborate seamlessly and ensures consistent rendering and output.

- **Improved Efficiency**: DevOps practices, along with Docker, Jenkins, and Kubernetes, streamline the development, testing, and deployment processes, leading to faster delivery of Maya projects.

By incorporating Docker, Jenkins, and Kubernetes into the DevOps workflow for Autodesk Maya, you can achieve efficient and scalable development, testing, and deployment processes. This enables better collaboration among teams, ensures consistent environments, and optimizes the rendering and processing of Maya projects.
# Prerequisites

To run this project, make sure the following items are installed on your system:

- [Docker](https://www.docker.com/get-started): Docker is a containerization platform that enables you to package and run applications in isolated containers.

- Maya Installer: You need the appropriate Maya installer for your operating system. You can obtain the installer from Autodesk or a reliable source.

## Installation Instructions

Please follow the steps below to install and run the project:

1. Install Docker by following the instructions specific to your operating system available on the [Docker website](https://www.docker.com/get-started).

2. Download the Maya installer for your operating system from [Autodesk](https://www.autodesk.com/products/maya/overview) or another reliable source.

3. Place the Maya installer in the `maya` folder.

4. Ensure that the non-admin user has the appropriate rights to run Docker.

Please follow these instructions to install the necessary prerequisites and run the project.

## Environment Variables

To run this project, you will need to add the following environment variables to your `.env` file

`USER` : set the username inside the container

`DISPLAY` : to allow the Maya application to display its graphical interface on the host machine.


## Run Locally

Clone the project

```bash
  git clone https://github.com/avict0r/devops-maya
```

Go to the project directory

```bash
  cd devops-maya
```

Build and run the Docker container

```bash
  docker-compose up -d
```

Access the Maya container in interactive mode

```bash
  docker-compose exec -it maya bash
```

## Authors

- [@alainVictor](https://www.github.com/avict0r)
