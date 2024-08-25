## Create Dockerfile
## Build Docker image 
docker build -t springboot-docker-demo .
### ...tagging images
docker build -t springboot-docker-demo:0.1.RELEASE .
## Run Docker image in a Container
docker run -p 8080:8080 -d springboot-docker-demo
### to get the logs take the first 4 numbers of process id
docker logs -f 1234 
## Push Docker image into Docker Hub
Write in Console:
1. docker login
#### // Tag the docker image with the Docker ID 
2. docker tag springboot-docker-demo erickjd79/springboot-docker-demo:0.1.RELEASE
#### // Push the tagged image to docker hub repository (before it can be listed: docker images 
3. docker push erickjd79/springboot-docker-demo:0.1.RELEASE
