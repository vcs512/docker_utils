# Basic commands

## Run command inside a container
    docker container run -flags image command

### Examples:    
    docker container run -t ubuntu top

    docker container run --detach --publish 8080:80 --name nginx nginx

\--t: has its own TTY

\--detach: container runs in background

\--publish: map port 8080 (localhost) to 80 (container)

\--name: give name to use instead of ID


## See active containers
    docker container ls

## Contact container
    docker exec -flags IDcontainer command

Example:

    docker exec -it a1e bash

## Stop containers
    docker stop ID
    docker stop name

Example:

    docker stop a1e
    docker stop nginx mongo

## Delete non running images
    docker system prune

## See image list
    docker image ls

## Remove image downloaded
    docker image rm ID

## Build image
    docker build -t name:tag