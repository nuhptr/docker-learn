# FROM COMMAND

The `FROM` command is used to set the base image for the Dockerfile. The `FROM` command must be the first command in the Dockerfile.

```bash
FROM image[:tag] [AS name]

# Example
FROM ubuntu:20.04 (Set the base image to Ubuntu 20.04)
```

# WORKDIR COMMAND

The `WORKDIR` command is used to set the working directory for any `RUN`, `CMD`, `ENTRYPOINT`, `COPY` and `ADD` instructions that follow it in the Dockerfile.

```bash
WORKDIR /path/to/workdir

# Example
WORKDIR /app (Set the working directory to /app)
```

# COPY COMMAND

The `COPY` command is used to copy files or directories from the host system to the container.

```bash
COPY [--chown=<user>:<group>] <src>... <dest>

# Example
COPY . /app (Copy all files from the current directory to /app in the container)
```

# RUN

The `RUN` command is used to execute commands in the container.

```bash
RUN <command>

# Example
RUN npm run dev (Run the npm run dev command in the container)
```

# EXPOSE

The `EXPOSE` command is used to expose a port from the container to the host system.

```bash
EXPOSE <port> [<port>/<protocol>...]

# Example
EXPOSE 3000 (Expose port 3000 from the container to the host system)
```

# ENV

The `ENV` command is used to set environment variables in the container.

```bash
ENV key=value

# Example
ENV NODE_ENV=production (Set the NODE_ENV environment variable to production)
```

# ARG

The `ARG` command is used to define build-time variables in the Dockerfile.

```bash
ARG <name>[=<default value>]

# Example
ARG NODE_VERSION=14 (Define a build-time variable NODE_VERSION with a default value of 14)
```

# VOLUME

The `VOLUME` command is used to create a mount point in the container.

```bash
VOLUME ["/data"]

# Example
VOLUME /myvol (Create a mount point at /myvol in the container)
```

# CMD

specify the command that should be executed when a container is launched from the Docker image

```bash
CMD ["executable","param1","param2"] (exec form, this is the preferred form)

CMD npm run dev
```
