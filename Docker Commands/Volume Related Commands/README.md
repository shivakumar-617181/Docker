
docker volume and ports:-

docker volume ls 
Used to list docker volumes

docker volume create (volumeName)
This Command used to create the docker volume 

docker volume inspect (volumeName)
This Commmand is Used to show about docker volume metadata

docker volume purne
To Delete all volumes which are not attached to a container

docker run -v (hostdirectorypath):(containerdirectory) (imageName)
This Command is Used to attach container directory path host local path. so that Our data will be Secured in the Host Path.
