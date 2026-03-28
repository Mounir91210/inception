# Developer Documentation

## Environment Setup

## Prerequisites
- Docker
- Docker Compose
- Make

## Project Structure

.
├── docker-compose.yml
├── Makefile
├── srcs/
│ ├── requirements/
│ ├── nginx/
│ ├── wordpress/
│ └── mariadb/

## Configuration

Environment variables are defined in:

.env


Secrets are stored in:

secrets/


### Build and Run

make all

This will :

- Build Docker images
- Create containers
- Start services

To Stop Containers :
- make stop

To Clean Project :
- make fclean

### Useful Commands

List containers:
-docker ps -a

Access a container:
-docker exec -it <container_name> bash

View logs:
-docker logs <container_name>

### Data Persistence

Data is stored using Docker volumes.

To list volumes:
- docker volume ls

Volumes ensure that data (database, WordPress files) persists even if containers are removed.