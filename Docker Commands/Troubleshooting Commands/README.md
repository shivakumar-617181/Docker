Troble Shooting Commands:-
docker logs (containerName)
It will shows the container logs related to container.

docker logs -f (containerName)
It Will shows the logs related to container in real time

docker logs -t (containerName)
It Will shows the logs related to container in real time with time stamps

docker inspect (containerName)
It will shows the details/metadata about the container.

docker top (containerName)
It will shows all the processes related to the container.

docker stats (containerName)
It will shows the resources (CPU,RAM) Usage related to the Container.

docker diff (containerName)
It will shows the any files are changes since container StartUp

docker run -d --name (containerName) (imageName) (command) 
docker attach (containerName) 
This Command is Used to attch a command to container and see output related to that container inside of our container.

docker exec -it (containerName) /bin/bash
It is used into container terminal 

docker system info
This Command is used to display system wide information

docker system purne
This Command is Used to delete
all Stopped containers

Unused networks

Dangling images (not tagged or used by any container)

Build cache

