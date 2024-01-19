# Openapi: Generated CurrentAccount Stub API
 
This Spring-boot project generates a unimplemented API stub based on the [CurrentAccount.yaml](https://github.com/mpirotaiswilton-IW/OpenAPI-generator-Springboot/blob/main/openapi-current-account-stub/src/main/resources/CurrentAccount.yaml "link to file in GitHub repository") file. The solution can be dockerized alongside a Postgres SQL Database and PGAdmin container. Since the API is a stub, it does not contain any functional component, though it can be run and tested without functionality. 

### Summary

[Openapi: Generated CurrentAccount Stub API](#openapi-generated-currentaccount-stub-api)
* [Summary](#summary)
* [Setup and Pre-requisites](#setup-and-pre-requisites)
* [Deployment](#deployment)
    * [Deploy the API into a docker container:](#deploy-the-api-into-a-docker-container)
        * [Using Docker Compose](#using-docker-compose)
        * [By building an image, then creating a container](#by-building-an-image-then-running-it)
* [Testing](#testing)

## Setup and Pre-requisites

1. If not already installed:

-  Install Docker on your device (you can use the following link for a guide: [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/))
- Install the latest version of OpenJDK 17 on your device (The following page has a complete catalogue of OpenJDK downloads: [https://www.openlogic.com/openjdk-downloads](https://www.openlogic.com/openjdk-downloads))

2. Clone this repository or download the .zip file from GitHub (extract the downloaded zip file )

## Deployment

1. Using a Command Line Interface used to run Docker and docker-compose commands, change directory to the downloaded/cloned repository then change directory to the `openapi` folder.

2. Create a .jar file of the API by running the following command:

```
./mvnw clean package
```

### Deploy the API into a docker container:

#### Using Docker-compose:
Run the following command: 

```
docker-compose up --build
```
#### By building an image, then creating a 

Run this command:

```
docker build -t openapi . 
```

Then run the following command:
```
docker run --name openapi-app openapi
```
---

A docker container called `openapi-app` should now be running and ready for use.

## Testing

1. With a web browser of your choice, navigate to <http://localhost:8080/swagger-ui/index.html>
2. On this page, you'll see every endpoint that the API stub has available
3. Select the `/CurrentAccount/{currentaccountid}/Retrieve` enpoint and then select the `Try it out` button
4. Fill in the `currentaccountid` parameters with a number greater than 0, then press the blue `Execute` button. This should yield a `501 Unimplemented` response code