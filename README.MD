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
### Start container with open ports and interactive mode
> docker run -it -p 3000:3000 CONTAINER_ID
### Start container with volumes (reference to our own current folder)
> docker run -it -p 3000:3000 CONTAINER_ID

### Start container with volumes - preserve node_modules - active watcher for changes
> docker run -it -p 3000:3000 -v /app/node_modules -v /c/Users/username/frontend:/app -e CHOKIDAR_USEPOLLING=true CONTAINER_ID

### Start container without enviroment variable (can be added to package.json if react)
> docker run -it -p 3000:3000 -v /app/node_modules -v C:\Users\Jacob\GithubProjects\reactContainer\frontend:/app twizzx/reactdevelopment

### Ssh to running container (depends on OS)
> docker exec -it 2d7bc51163a2 /bin/sh

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
### Show containers from the current directory
docker-compose ps