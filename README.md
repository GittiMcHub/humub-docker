# humub-docker

Builds docker containers for humhub with persitence

# Status
- not finished yet
- uses db root user
- set up for http only

# Prerequisites
- Docker
- Docker compose

# Start

1. Create your .env file
Sample:
```
MYSQL_ROOT_PASSWORD=somerootpassword
HUMHUB_DB_NAME=humhub
HUMHUB_DB_USER=root
HUMHUB_DB_PASSWORD=somerootpassword
HTTP_HOSTNAME=localhost
HTTP_PORT=80
```
2. Start with docker-compose
```
docker-compose up
```
