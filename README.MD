# Docker Notes

## TLDR
When you've a dockerfile, you must build and run it to make use of it.
- Dockerfile will make sure we build a container, to setup a OS for our application. This is also where we can setup network to our other containers

- Docker-composer can automate our docker build and boot up our containers. This makes it easy, if we are dependent on other containers and if there are multiple.




## Docker

### Show all running containers
> docker ps

### Stop specified container
> docker stop $id
### Start specified container
> docker run  $id

### Build docker from this folder without name
> docker build .
### Build docker from this folder with name
> docker build -t twizzx/visits:latest .


## Docker-composer
### Build from docker-composer.yml
docker-compose build
### Run docker-composer containers
docker-compose up
### Stop docker-composer containers
docker-compose down
### Build and run rocker composer containers
docker-compose up --build