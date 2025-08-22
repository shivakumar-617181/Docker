**Docker Commands:-**

**Docker Image Related Commands:-**

**docker images**

Displays the all Images

**docker search (imageName)**

Used to Search for a Image.

**docker pull (imageName)**

Used to Pull a Image From Remote Registry to Local Docker Server

**docker push  (registryname/reponame):tag**
This Command is Used to Push the Local Built Image to Remote Repository.

**docker build -t (registryname/reponame):tag .**

This Command is Used to Build the Docker Image From the Dockerfile.  when the Docker File is Present Inside the Same Directory.

**docker build -t (registryname/reponame):tag -f (pathpathofdockerfile)**
This Command is Used to Build the Docker Image From The Dockerfile. When Docker file Is Present In Another Directory.

**docker rmi (imagename):tag**
Command is Used to Remove the image

**docker inspect (imageName)**
This Command is Used to Inspect / to view the layers Information about the docker Image.

**docker image purne**
To Remove all unused docker Images.
