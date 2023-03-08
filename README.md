
# Directus deployment on kubernetes from docker-compose.yml and custom Dockerfile

This docker image is customized with the spatialite extension and a patch fixing this issue:
https://github.com/directus/directus/issues/17002

Docker image name:
ghcr.io/noops-land/directus-k8s:latest

## Local development on macOS

```sh
npm install
npm start
```

## Local development with docker compose

```sh
docker-compose up --build
```

## Docker image building from github action

On every commit on the main branch of this git repo, the workflow in .github/workflows is executed.

This github action updates the docker image in:
pkgs/container/directus-k8s

## Installation on kubernetes
```sh
npm run install-k8s
```

## Deployment on kubernetes
```sh
npm run deploy-k8s
```
