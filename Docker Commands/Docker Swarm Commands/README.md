**Docker Swarm Related Commands:-**

docker swarm init

The Command Is Used to Initialize a Docker Swarm Cluster. It Turns The Current Docker Host Into a Manager node. And It Will Prints The Manger and Worker Token.

docker service create --name (serviceName) --mode global -p (hostPort):(containerPort) (imageName)

This Command Is Used to Create a Service with Particular Image and Define The Port Specification.

docker inspect (serviceName)

It will tells the details about the Service Name.

docker node ls

It will Displays the Available nodes for the Cluster.

docker Service ls

It will Displays the Services Which are Deployed Into The Cluster.

docker node ps (node-name)

This Command will displays the containers which are running In the node deployed using the service.

docker service ps (service-name)

This Command Will Displays The Containers Which Are Running For The Particular Service.

docker service rm (service-name)

This Command is used to remove the Service.

docker node rm (node-name)

This Command is used to remove the node from the Cluster.

docker service scale (service-name)=(desired number of replicas)

This Comand is used to scale the Replicas for respective Service.

docker node update (node-name) --label-add (key)=(value)

This Command is Used to Update/add the label for the Cluster.
