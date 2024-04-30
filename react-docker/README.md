# React + Docker

This is a simple React app that is containerized using Docker. The app is built using the `bun create vite@latest` CLI tool.

## Helper

-  add --host in package.json at "dev" script to run the app in the container

# DOCKER COMMANDS

-  `docker build -t react-docker .` (Builds the Docker image with the tag `react-docker` and the current directory as the build context)
-  `docker run -p 5173:5173 react-docker` (Runs the Docker container with the image `react-docker` and maps port 5173 of the host to port 5173 of the container)

For watching changes create volume and run this command:

```bash
docker run -p 5173:5173 -v $(pwd):/app -v /app/node_modules react-docker
```

To share the local to hub docker repository:

-  `docker login` (Login to Docker Hub)
-  `docker tag react-docker <docker-hub-username>/react-docker` (Tag the Docker image with the Docker Hub username)
-  `docker push <docker-hub-username>/react-docker` (Push the Docker image to Docker Hub)
