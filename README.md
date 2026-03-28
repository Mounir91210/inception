*This project has been created as part of the 42 curriculum by modavid.*

# Inception

## Description
This project aims to introduce system administration using Docker.  
The goal is to set up a small infrastructure composed of multiple services running in containers.

The project includes services such as:
- NGINX
- WordPress
- MariaDB

Each service runs in its own container and communicates through a Docker network.

## Instructions

### Prerequisites
- Docker
- Docker Compose
- Makefile

### Installation & Launch
```bash
- To start the project
        make all
- To stop the project
        make stop
- To clean everything
        make clean
```
### Resources
- Docker documentation: https://docs.docker.com/
https://blog.stephane-robert.info/docs/conteneurs/moteurs-conteneurs/docker/

- WordPress documentation: https://wordpress.orgsupport/

- NGINX documentation: https://nginx.org/

- Mariadb documentation: https://mariadb.com/docs

- AI Usage
    Understanding Docker concepts
    Debugging configuration issues
    Generating documentation structure

### Docker & Design Choices
Why Docker

Docker allows lightweight, portable, and reproducible environments compared to virtual machines.

- Virtual Machines vs Docker
    VM: full OS, heavy, slower
    Docker: lightweight, faster, shares host kernel

- Secrets vs Environment Variables
    Environment variables: easy but less secure
    Docker secrets: safer, used for sensitive data (passwords, credentials)

- Docker Network vs Host Network
    Docker network: isolated, secure communication between containers
    Host network: direct access to host network (less isolation)

- Docker Volumes vs Bind Mounts
    Volumes: managed by Docker, better for persistence
    Bind mounts: linked to host filesystem, more flexible but less portable

All code and configurations were reviewed and tested manually.