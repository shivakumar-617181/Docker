**Docker Commands:-**

**Docker Image Related Commands:-**

**docker images**

Displays the all images

docker search (imageName)
Used to search for a Image.

docker pull (imageName)
Used to pull a Image from remote registry to local Docker host

docker push  (registryname/reponame):tag
This Command is Used to Push the local built image to remote repository.

docker build -t (registryname/reponame):tag .
this command is Used to build the docker image from the Dockerfile. This Command is used docker file is present inside the same directory.

docker build -t (registryname/reponame):tag -f (pathpathofdockerfile)
this command is Used to build the docker image from the Dockerfile. This Command is used if Docker file is present in another directory.

docker rmi (imagename):tag
Command is Used to Remove the image

docker inspect (imageName)
This Command is Used to Inspect / to view the layers Information about the docker Image.

docker image purne
To Remove all unused docker Images.
