<!-- This is palce where i'll start making notes about the notes of DEvops from scratch for beginner -->
# DevOps Notes
## Introduction to DevOps
DevOps is a set of practices that combines software development (Dev) and IT operations (Ops). The main goal is to shorten the systems development life cycle and provide continuous delivery with high software quality.

<!-- 9 phases of Devops -->
## Phases of DevOps
1. **Planning**: Define the project scope, requirements, and objectives.
2. **Development**: Write and build the code.
3. **Testing**: Validate the code through automated and manual testing.
4. **Deployment**: Release the code to production environments.
5. **Monitoring**: Continuously monitor the application and infrastructure for performance and issues.
6. **Feedback**: Gather feedback from users and stakeholders to improve the product.
7. **Operations**: Manage the infrastructure and ensure system reliability.
8. **Security**: Integrate security practices throughout the DevOps lifecycle (DevSecOps).
9. **Collaboration**: Foster a culture of collaboration between teams to enhance communication and efficiency.

## Key Concepts
- **Collaboration**: DevOps emphasizes collaboration between development and operations teams.
- **Automation**: Automating repetitive tasks to improve efficiency and reduce errors.
- **Continuous Integration (CI)**: Merging code changes frequently to detect issues early.
- **Continuous Delivery (CD)**: Ensuring that code changes are automatically prepared for a release to production.
- **Infrastructure as Code (IaC)**: Managing infrastructure using code and automation tools.
## Tools and Technologies
- **Version Control Systems**: Git, GitHub, GitLab
- **CI/CD Tools**: Jenkins, Travis CI, CircleCI
- **Configuration Management**: Ansible, Puppet, Chef
- **Containerization**: Docker, Kubernetes
- **Monitoring and Logging**: Prometheus, Grafana, ELK Stack

<!-- starting with docker -->
## Docker
Docker is a platform that enables developers to automate the deployment of applications inside lightweight, portable containers. Containers package an application and its dependencies, ensuring consistency across different environments.
<!-- need of docker -->
### Why Use Docker?
- **Portability**: Run containers on any system that supports Docker without worrying about dependencies.
- **Isolation**: Each container runs in its own environment, preventing conflicts between applications.
- **Scalability**: Easily scale applications by running multiple containers.
- **Efficiency**: Containers share the host OS kernel, making them lightweight and fast to start.


### Key Concepts
- **Images**: Read-only templates used to create containers.
- **Containers**: Lightweight, portable instances of applications running in isolated environments.
- **Dockerfile**: A script containing instructions to build a Docker image.
- **Docker Compose**: A tool for defining and running multi-container Docker applications.

### Basic Commands
- `docker run`: Create and start a container.
- `docker ps`: List running containers.
- `docker stop`: Stop a running container.
- `docker build`: Build a Docker image from a Dockerfile.
- `docker-compose up`: Start all services defined in a `docker-compose.yml` file.
<!-- more commands like images,history,delete,pull -->
- `docker images`: List all Docker images.
- `docker rmi`: Remove a Docker image.
- `docker pull`: Download a Docker image from a registry.
- `docker exec`: Execute a command in a running container.
<!-- more commands related to the docker  container start stop restart with container ID-->
- `docker rm`: Remove a stopped container.
- `docker inspect`: View detailed information about a container or image.
- `docker network ls`: List all Docker networks.
- `docker volume ls`: List all Docker volumes.
- `docker start`: Start a stopped container.
- `docker restart`: Restart a running or stopped container.
- `docker logs`: View the logs of a container.
- `docker network`: Manage Docker networks.
<!-- what is inractive and terminal and detached mode in docker -->
### Running Containers
- **Interactive Mode**: Use `docker run -it <image>` to run a container interactively, allowing you to access the terminal.
- **Detached Mode**: Use `docker run -d <image>` to run a container in the background, allowing it to run independently of the terminal.

<!-- what is dockerfile -->
A Dockerfile is a text file that contains instructions for building a Docker image. It defines the environment in which an application runs, including the base image, dependencies, and configuration.
<!-- what is base imagee -->
### Base Image
A base image is the starting point for building a Docker image. It can be an official image
from Docker Hub or a custom image. Base images provide the necessary environment and libraries for your application to run.
<!-- type of base image(Full os base iamge, language runntime image and scratch empty) -->
### Types of Base Images
1. **Full OS Base Image**: Contains a complete operating system (e.g., Ubuntu, CentOS).
2. **Language Runtime Image**: Includes a specific programming language runtime (e.g., Python, Node.js).
3. **Scratch**: An empty base image used to build minimal images from scratch, often used for small, single-purpose applications.
<!-- multi stage building -->
### Multi-Stage Builds
Multi-stage builds allow you to create smaller, more efficient Docker images by separating the build environment from the runtime environment. This reduces the final image size by excluding unnecessary build dependencies.

### Basic Dockerfile Structure
```dockerfile
# Use an official base image
FROM <base_image>
# Set the working directory
WORKDIR /app
# Copy files from the host to the container
COPY . .
# Install dependencies
RUN pip install -r requirements.txt
# Expose a port
EXPOSE 5000
# Define the command to run the application
CMD ["python", "app.py"]
```

### Example Dockerfile
```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "app.py"]
```
### Example docker-compose.yml
```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/app
  db:
    image: postgres:latest
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
```
