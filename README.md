# CS3219-A

# How to run the docker container

## Get docker images

Get the docker image from docker hub using the command

    docker pull dargoyaki/cs3219a

Then, build the image from the Dockerfile using the command

    docker build -t dargoyaki/cs3219a .

## Running the container without reverse proxy

Once cs3219a iamge is up, run the following command

    docker run -p 8888:5000 --name cs3219a dargoyaki/cs3219a

The html page (sentence generator) is now accessible on http://localhost:8888

## Running the container with reverse proxy

To do this, you need to clone the repo first to get all the files.

Pull the Nginx image first using the command

    docker pull nginx

Then, assuming that the cs3219a image has already been created, run docker compose using the command

    docker-compose up -d nginx

ensure that Nginx service is created first to test out the dependency

The html page will now be accessible on http://localhost:80 :)
