**Docker Troubleshooting Commands:-**


**docker logs (containerName)**

It will shows the container logs related to container.

**docker logs -f (containerName)**

It Will shows the logs related to container in real time

**docker logs -t (containerName)**

It Will shows the logs related to container with time stamps

**docker inspect (containerName)**

It will shows the details/metadata about the container.

**docker top (containerName)**

It will shows all the running Processes Related to The Container.

**docker stat (containerName)**

It will shows the resources Consumption (CPU,RAM) related to the Running Container.

**docker diff (containerName)**

It will shows the any files are changes since container StartUp

docker run -d --name (containerName) (imageName) (command) 
**docker attach (containerName)** 
This Command is Used to attch a Command to container and see Output Related to that Container Inside of Our Container Terminal.

**docker exec -it (containerName) /bin/bash**

It is used enter into Running Container Terminal 

**docker system info**

This Command is Used to Display System Wide Information

**docker system purne**

This Command is Used to Delete All Stopped Containers, Unused networks, Dangling images (not tagged or used by any container), Previous Build Cache.

Build cache

