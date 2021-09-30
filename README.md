# Traefik JWT Auth
Traefik forward auth implementation to validate json web tokens.

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/dot-base/traefik-jwt-auth)](https://github.com/dot-base/traefik-jwt-auth/releases)
[![Docker Build Status](https://img.shields.io/badge/We%20love-Docker-blue?style=flat&logo=Docker)](https://github.com/orgs/dot-base/packages)


## Usage

Want a Traefik JWT Auth of your own? The easiest way is to deploy our docker container. Just follow the steps below to get started.


### Requirements
- [Docker Engine >= v1.13](https://www.docker.com/get-started)

### Deployment
1. [optional] Set environment variables to configure the container:
    ```sh
    export KEYCLOAK_REALM_URL=http://keycloak:8080/auth/realms/dotbase
    ```
1. Start the container
    ```
    docker run --name traefik-jwt-auth -p 3000:3000 -d ghcr.io/dot-base/traefik-jwt-auth:latest
    ```
1. Done and dusted 🎉. The Server is available on port 3000.


## Configuration

### Environment Variables

| Variable Name | Default |
| --- | --- |
| KEYCLOAK_REALM_URL | http://keycloak:8080/auth/realms/dotbase |
| git diff | Show file differences that haven't been staged |


## Contributing

This project is written in Typescript. For an introduction into the language and best practices see the [typescript documentation](https://www.typescriptlang.org/docs/home.html).

### Requirements
- [Node.js >= v16](https://nodejs.org/en/)
- A local copy of this repository

### Running Locally
1. Install all dependencies
    ```
    npm install
    ```
1. Set the environment variables:
    ```
    export KEYCLOAK_REALM_URL=http://127.0.0.1:8080/auth/realms/dotbase
    ```
1. Start the development server
    ```
    npm start
    ```
1. After some startup the server will be available at http://localhost:3000.
1. Go and mix up some code 👩‍💻. The server will reload automatically once you save. Remember to keep an eye on the console.

