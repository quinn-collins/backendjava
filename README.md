# Backend Java

Quick project utilizing Spring framework to stand up a REST API utilizing best practices and HATEOAS

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Coming soon..
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Coming soon..
```

## Running the application locally

With Maven installed you can run the application with the following command
```
./mvnw package && java -jar target/backendjava-0.0.1-SNAPSHOT.jar
```

### Running within Docker container

With Docker installed you can run the application within a docker container with the following command
```
docker run --name backend_rest_api -d -p 8080:8080 -t quinnc11/backendjava
```

### Building and pushing Docker image manually

With Maven installed you can build a docker image locally and push it utilizing the following commands
```
./mvnw install dockerfile:build
./mvnw dockerfile:push
```
You should only need to push the image if you are building your own custom version. You won't need to build the image unless you don't want to pull it from my repository on Docker Hub.

## Testing API manually

You can test the application the same way you do with any other API.

With CURL
```
curl localhost:8080/employees
curl localhost:8080/employees/1
curl -X POST \
  http://localhost:8080/employees \
  -H 'Content-Type: application/json' \
  -d '{
    "name": "xyz",
    "role": "xyz"
}'
curl -X PUT \
  http://localhost:8080/employees/3 \
  -H 'Content-Type: application/json' \
  -d '{
    "name": "zyx",
    "role": "zyx"
}'
curl -X DELETE http://localhost:8080/employees/2
curl http://localhost:8080/orders
curl -X DELETE http://localhost:8080/orders/4/cancel
curl -X PUT http://localhost:8080/orders/4/complete
curl http://localhost:8080/orders/3
curl -X POST \
  http://localhost:8080/orders/ \
  -H 'Content-Type: application/json' \
  -d '{
    "description": "abc"
}'
```

## Running the unit tests

Running unit tests coming soon

```
Coming soon..
```

### Running integration/end-to-end/automation tests

Running automation tests coming soon

```
Coming soon..
```

## Deployment

Coming soon..

## Authors

* **Quinn Collins** 

## Acknowledgments

* https://spring.io/guides/gs/spring-boot-docker/ 
* Coming soon..
* Coming soon.. 
