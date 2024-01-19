# Openapi: Generated CurrentAccount Stub API
 
This Spring-boot project generates a unimplemented API stub based on the [CurrentAccount.yaml](https://github.com/mpirotaiswilton-IW/OpenAPI-generator-Springboot/blob/main/openapi-current-account-stub/src/main/resources/CurrentAccount.yaml "link to file in GitHub repository") file. The solution can be dockerized alongside a Postgres SQL Database and PGAdmin container. Since the API is a stub, it does not contain any functional component, though it can be run and tested without functionality. 

### Summary

[Openapi: Generated CurrentAccount Stub API](#openapi-generated-currentaccount-stub-api)
* [Summary](#summary)
* [Setup and Pre-requisites](#setup-and-pre-requisites)
* [Testing](#testing)

## Setup and Pre-requisites

1. If not already installed:

-  Install Docker on your device (you can use the following link for a guide: [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/))
- Install the latest version of OpenJDK 17 on your device (The following page has a complete catalogue of OpenJDK downloads: [https://www.openlogic.com/openjdk-downloads](https://www.openlogic.com/openjdk-downloads))

2. Clone this repository or download the .zip file from GitHub (extract the downloaded zip file )

## Deployment

1. Using a Command Line Interface used to run Docker and docker-compose commands, change directory to the downloaded/cloned repository then change directory to the `openapi` folder.

2. Run the following command: 

```
docker-compose up --build
```

3. 3 docker containers should now be running:
    * `openapi-app`: where the spring-boot api image, built using a Dockerfile, is containerized
    * `db`: where a Postgres database is containerized and used by the API
    * `openapi-pgadmin`: where a pgAdmin interface is containerized. This is used to monitor our Postgres database container

## Testing

1. With a web browser of your choice, navigate to <http://localhost:8080/swagger-ui/index.html>
2. On this page, you'll see every endpoint that the API stub has available
3. Select the `/CurrentAccount/{currentaccountid}/Retrieve` enpoint and then select the `Try it out` button
4. Fill in the `currentaccountid` parameters with a number greater than 0, then press the blue `Execute` button. This should yield a `501 Unimplemented` response code