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
`docker run --name nodejs-7-instance -t nodejs-7`<br />
`docker run -d -p 3001:3001 nodejs-7`<br />
`docker run -d -p 3001:3001 --name nodejs-7-instance -t nodejs-7`<br />
`docker run -d -p 3001:3001 --name nodejs-7-instance nodejs-7`<br />
`docker run -d --net=host --name nodejs-7-instance nodejs-7`

### Start a container
`docker start <container name | container id>`

examples:<br />
``docker start `docker ps -q -l` ``<br />
`docker start nodejs-7-instance`

## Links
### Docker official documentation
https://docs.docker.com/engine/reference/run/<br />
https://docs.docker.com/engine/reference/commandline/cli/<br />
https://docs.docker.com/engine/reference/builder/<br />
https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/
