# Docker CICD 
Repo for some personal docker tests for automating some stuff.

## Workflows
Currently containing two workflows to build and push a docker image to `ghcr` and `DockerHub` every time a new tags created and pushed (e.g. by using `git tag ...` & `git push --follow-tags`)

The images can be pulled from here:

### GitHub Container Registr (`ghcr`)

```shell
docker pull ghcr.io/hbertsch/docker-cicd:latest
```

### Docker Container Registr (`DockerHub`)

```shell
docker pull hbertsch/docker-cicd:latest
```

## Demo Program 

This little program collects data (in this case quotes) from an API by using the `requests` python package and saves the collected data to a `Docker Volume`. The `volume` will be auto-created if you use the provided `Docker Compose`file to run the container.

### Run container using `Docker Compose`

Docker compose will consume either the `Dockerfile` or pull the image from one of the provided `container registries`(depending which one you comment in/out in the `Dockercompose`file). The only thing you need to do after checking out this repo is to `cd`into the root dir and type

```shell
docker compose up
```

