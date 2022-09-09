# Docker Compose LEMP Stack

This repository contains docker configuration to start a LEMP (Linux, Nginx, MariaDB, PHP) stack.

## Details
The following containers are used.

 - one container for Nginx;
 - one container for PHP (7.4 PHP-FPM);
 - one container for MySQL (8);
 - one container for phpMyAdmin.

## Configuration
The Nginx configuration can be found in `docker/nginx/`

The php configuration can be found in `docker/php/`

The Mysql data can be found in `docker/mysql/data`

### Environment variables, for example in the included .env file:

| Key | Description                                              |
|-----|----------------------------------------------------------|
| DOCKER_PREFIX | The name used when creating a container.                 |
| DB_ROOT_PASSWORD | The MySQL root password used when creating the container |
| PORT_NGINX | Web port|
| PORT_PHP | PHP port|
| PORT_MYSQL | DB port|
| PORT_PMA | PhpmyAdmin|

## Usage
To use it, simply follow the following steps:

### Clone this repository.
`git clone https://github.com/aradikdev/docker-lemp.git`

### Start the server (inside the directory you just cloned)
`docker-compose up -d`

## Entering the containers

`docker exec -ti {CONTAINER_NAME} bash`

{APP_NAME}-php
{APP_NAME}-nginx
{APP_NAME}-mariadb
