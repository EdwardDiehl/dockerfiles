# https://docs.docker.com/engine/reference/builder/
# https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/

# The FROM instruction sets the Base Image for subsequent instructions.
# As such, a valid Dockerfile must have FROM as its first instruction.
# The image can be any valid image – it is especially easy to start by pulling an image from the Public Repositories.
FROM node:7

# The RUN instruction will execute any commands in a new layer on top of the current image and commit the results.
# The resulting committed image will be used for the next step in the Dockerfile.
RUN mkdir -p /usr/src/app

# The WORKDIR instruction sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile.
# If the WORKDIR doesn’t exist, it will be created even if it’s not used in any subsequent Dockerfile instruction.
WORKDIR /usr/src/app

# The COPY instruction copies new files or directories.
COPY package.json /usr/src/app

RUN npm install

COPY . /usr/src/app

# The EXPOSE instruction informs Docker that the container listens on the specified network ports at runtime.
EXPOSE 3001

# Serve the app
CMD ["node", "server.js"]
