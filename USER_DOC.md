# User Documentation

## Services Overview

This project provides the following services:
- NGINX: handles HTTPS connections
- WordPress: website service
- MariaDB: database for WordPress

## How to Start and Stop the Project

```bash
    make all
    make stop
```

## Access the Website

Open your browser and go to:

    https://localhost
or
    https://login.42.fr

## Access the Administration Panel

WordPress admin panel:

    https://localhost/wp-admin
or
    https://login.42.fr/wp-admin

## Credentials Management

Credentials are stored using:

    Environment variables
    Docker secrets

You can find them in:

    .env

To Check Services Status :
- docker ps

To check logs:
- docker logs <container_name>