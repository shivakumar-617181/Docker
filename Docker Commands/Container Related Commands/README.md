docker ps
shows All Running Containers

docker ps -a 
Displays Running as Well As Stopped Containers

docker run -it --name=(desired Container Name) (imagename):tag
This Command is Used to Run A Container In Intarctive Mode

docker run -d --name=(desired Container Name) (imagename):tag
This Command is Used to Run A Container In detach Mode

docker stop
This Command is Used to Stop The Container

docker kill
This Command is Used to kill a Container.


docker container related commands:-

docker run -d -p --name=(containerName) (hostport):(containerport) (imageName)
This Command is used to run a container in detach mode.

docker ps 
It will 

docker ps -a

docker ps -q
It will lists the only running containers IDs

docker ps -aq
It will lists the all containers IDs including (stopped and running)

docker restart (container name/ID)
It will restart the container 

docker stop (container/ID)
It will stops the container.Allows grace period

docker kill (container ID)
It will kills container with out grace period.

docker rm -f (containerName)
It will removes the container forcefully.

docker cp (containerName):(path of container directory/file) (hostpath)/(file/directoryName)
Used to copy files from local host directory to running container path.

docker rm -f $(docker ps -aq --filter status="exited")
It will delete all the stooped containers. 

docker ps -aq --filter status="paused"
It will display the all paused containers.
