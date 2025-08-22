**Docker Swarm:-**

Docker Swarm is a Docker Native Container Orchestration Engine Built On Top of Docker Engine. It Allows You to Manage a Cluster of Docker Nodes as a single, Unified System, Enabling the Deployment, Scaling, Rolling Updates, Fault Tolerate, High Availability, Service discovery, Load balancing and Management of Containerized Applications Across Multiple Machines.

**Note:-** 

1). In the Docker Swarm Method, The Containers Are Managed In The Form Service. Service Is Responsible for the Scalling, Fault tolerate, Service Discovery, Load Balancing Of The Containers.
2). For the Containers, the Container Management resources like Networking, Persistent Data like Volumes Details are Deployed in the Docker-Compose.yml file. (Sample docker compose volume file is pasted below).
3). The Swarm Follows the Client Server and Node Architecture.
     CLI    --> Where Client will Executes The Commands
     Server --> Manages cluster state, Decides where to schedule containers. 
4). Volumes:- Used for Persistent Storage In Swarm Services.
5). Overlay Networks:- Allow Communication Between Services Across Nodes.


