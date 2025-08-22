**Container Related Commands:-**

**docker ps**

It will lists all Running Containers

**docker ps -a**

Displays the Running, as Well As Stopped Containers

**docker ps -q**

It will lists the only running containers IDs

**docker ps -aq**

It will lists the all containers IDs including (stopped and running)

**docker run -it --name=(desired Container Name) (imagename):tag**

This Command is Used to Run A Container In Intarctive Mode.

**docker run -d --name=(desired Container Name) (imagename):tag**

This Command is Used to Run A Container In detach Mode.

**docker stop (containerName)**
This Command is Used to Stop The Container. With Grace Period.

**docker kill (containerName)**

This Command is Used to kill a Container. WithOut Grace Period

**docker restart (container name/ID)**

It will restart the container 

**docker rm -f (containerName)**

It will removes the container forcefully.

**docker cp (containerName):(path of container directory/file) (hostpath)/(file/directoryName)**

It is Used to copy files from local host server directory to running container path.

**docker rm -f $(docker ps -aq --filter status="exited")**
It will delete all the stoped containers. 

**docker ps -aq --filter status="paused"**
It will displays the paused Containers.
It will display the all paused containers.
It will display the all paused containers.
