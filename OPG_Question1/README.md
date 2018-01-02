# Pre-interview test - answer to Question 1
Submitted by Nick Romney 2 January 2018

## Question
Create a docker-compose file using v2 format that will create an nginx web server and postgres database container which can communicate successfully.

### Approach
- Use an up-to-date Vagrant box with Docker tools installed
- Test connectivity to Nginx welcome page, and custom page
- Review logs to ensure that PostgreSQL comes up cleanly
- Validate the format of the docker-compose.yml file

### Tested with docker compose
Using Vagrant box envimation/ubuntu-xenial-docker

### Validated docker-compose.yml file by running

```docker-compose -f docker-compose.yml config```

