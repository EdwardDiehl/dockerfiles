# Docker playground
# This project is used to store Dockerfiles and provide docker command line and Dockerfile cheat sheet

## Stacks
### nodejs
* [node:7](nodejs/Dockerfile)

## Docker command line
### Build a docker image
`docker build -t <name> --file <docker file> <docker context dir>`

examples:<br />
`docker build -t nodejs-7 .`<br />
`docker build -t nodejs-7 . --no-cache=true`


### Create a container from an image and run it
`docker run --name <container name> -t <image name>`

examples:<br />
`docker run --name nodejs-7-instance -t nodejs-7`

## Links
### Docker official documentation
https://docs.docker.com/engine/reference/builder/<br />
https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/
