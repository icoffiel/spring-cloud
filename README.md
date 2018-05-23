# Spring Cloud Playground

## Config Server

This project is setup with a config first configuration. This means that each application will need to know the location of the config server in order to fetch it's config.

Each application is also setup to fail fast if the config server is not found. The `docker-compose` configuration ensures that each application will restart if they fail ensuring that eventually the services will come up assuming that the `config-service` is able to start.

## Building

*TODO:* Use gradle submodules to build all, or use a script to auto build everything needed.

1. Navigate into each project folder
1. run the following:
    ```
    // Windows
    gradlew.bat clean build
    
    // *nix
    ./gradlew clean build
    ```
1. Navigate to the root folder
1. Build the docker images:
    ```
    docker-compose build
    ```
    
## Running

1. Start the project:
    ```
    docker-compose up -d
    ```