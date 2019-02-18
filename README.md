# Backend Java

Quick project utilizing Spring framework to stand up a REST API utilizing best practices and HATEOAS

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* Maven
* Docker
* JVM

## Running the application locally

Clone or download the repository
```
git clone https://github.com/quinn-collins/backendjava.git
```

Use Maven to package the application and then run it with the java command
```
./mvnw package && java -jar target/backendjava-0.0.1-SNAPSHOT.jar
```

## Running within Docker container

Use Docker to run the application without needing to download or compile source code
```
docker run --name backend_rest_api -d -p 8080:8080 -t quinnc11/backendjava
```

## Building and pushing Docker image manually

### Build a Docker image
Using Maven you can build a docker image locally and then run it the same way you would pulling it from Docker Hub
```
./mvnw install dockerfile:build
docker run --name backend_rest_api -d -p 8080:8080 -t quinnc11/backendjava
```

### Push a Docker image
If you want to make changes to the source you can push the image you created up with the following command
```
./mvnw dockerfile:push
```

## Testing API manually

You can test the application the same way you do with any other API.

With CURL:
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

## Running integration/end-to-end/automation tests

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
