# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

## Getting Setup

> _tip_: this frontend is designed to work with the RestAPI backends). It is recommended you stand up the backend first, test using Postman, and then the frontend should integrate.

### Installing Node and NPM

This project depends on Nodejs and Node Package Manager (NPM). Before continuing, you must download and install Node (NPM is included) from [https://nodejs.com/en/download](https://nodejs.org/en/download/).

### How to run the apps

## Run the docker compose

Navigate to the udacity-c3-deployment/docker folder and run the following command.

```javascript
docker-compose -f docker-compose-build.yaml build --parallel
```

This builds the images.

Then you can run `docker-compose up` to test the app

Use postman script in this project to test the REST API.
The UI can also be tested if you navigate to http://localhost:8100/

# Deploy to Kubernetes cluster

Navigate to the folder udacity-c3-deployment/k8s

Run the following command

```
 kubectl apply -f frontend-deployment.yaml
 kubectl apply -f reverseproxy-deployment.yaml
 kubectl apply -f backend-user-deployment.yaml
 kubectl apply -f backend-feed-deployment.yaml
```

Docker images
https://hub.docker.com/r/petershodeinde/reverseproxy
https://hub.docker.com/r/petershodeinde/backend-feed
https://hub.docker.com/r/petershodeinde/backend-user
https://hub.docker.com/r/petershodeinde/frontend

TADA: everything is good to go
