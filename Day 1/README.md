# Guide for Day_1

Day 1 had me doing basic pod config using the docker image from docker hub.

The docker image is a Flask python file.

To run the *Flask_Docker-master* as a docker image, you could either build using the dockerfile in */Day 1/Flask_Docker-master/deployments/app/* or use the docker compose file in the *Day 1/Flask_Docker-master/deployments/*


## Using the Dockerfile to build our image

To use the Dockerfile, change directory into the folder which contains the Dockerfile, then run:

```cmd
docker build -it image_name .
```
The "." in the command is to ensure it uses the folder as the context for the build. You can change to the right context if your dockerfile is located in another directory. Ensure you use the right relative path for the build context.

The *image_name* is the name you want to the image to name the image after the build.

## Using Docker compose:

To use docker compose, change to the directory where the docker-compose file is located and run the command:
```cmd
docker compose up
```

_N:B_ To run the image as a container, use the command:
```cmd
docker run --name any_name_for_the_container -it name_of_image
```

You need not worry about port setting as the web application as the app will run on port 5000

# Running the built image in a Kubernetest Cluster

After building my image from the dockerfile/docker-compose file which I named Flask _flask_demo_, i pushed this image to the docker hub registry to enable me reuse it in future.

I will be using this image in my kubernetes cluster

I have the setup to run the image defined in _basic.yml file._ This runs a basic pod with an image.
