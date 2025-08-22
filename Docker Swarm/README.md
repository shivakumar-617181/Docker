**Docker Swarm:-**

Docker Swarm is a Docker Native Container Orchestration Engine Built On Top of Docker Engine. It Allows You to Manage a Cluster of Docker Nodes as a single, Unified System, Enabling the Deployment, Scaling, Rolling Updates, Fault Tolerate, High Availability, Service discovery, Load balancing and Management of Containerized Applications Across Multiple Machines.

**Note:-** 

**1).** In the Docker Swarm Method, The Containers Are Managed In The Form Service. Service Is Responsible for the Scalling, Fault tolerate, Service Discovery, Load Balancing Of The Containers.

**2).** For the Containers, the Container Management resources like Networking, Persistent Data like Volumes Details are Deployed in the Docker-Compose.yml file. (Sample docker compose volume file is pasted below).

**3).** The Swarm Follows the Client Server and Node Architecture.
     **CLI**    --> Where Client will Executes The Commands
     **Server** --> Manages cluster state, Decides where to schedule containers. 
     **Nodes:-**  --> Where Our Containers Will Run In The Cluster.
     
**4).** **Volumes**:- Used for Persistent Storage In Swarm Services.

**5).** **Overlay Networks**:- Allow Communication Between Services Across Nodes.

**6).**  Based On The **Labels and Constraints** and **Resource Availability** Manager  Will Decide Where to Schedule the Containers Inside The Cluster.

**7).** You Can Drain the Nodes, Manager For the Patching and Installing Updates In Our Cluster. 

**8).** Here The Scheduling of the Containers Have Two Modes.

       A). **Global-Mode:- **  One Container will Automatically Schedule the on Each Node. You Can`t Able to Setup the Scale-in and Scale-Down for the Global Replication Mode Containers. Most Suitable for Monitering, Logs and For Networking type of the Pods. 

       
       B). **Replica Mode:- **  All Our Application Containers are Deployed Into Clustrer in the Form Replica Mode. We Can Scal-up and Scale-down Based On the Load Getting For Our Pods. Based On the Replica Count Number Containers are Created In the Cluster.

Sample Dokcer-Compose file.   


------------------------------------

```
version: "3.8"

services:
  web: 
    image: nginx:latest # Image Name for Our Frontend Application
    ports:
      - "80:80" # Port Forwarding Section
    networks:
      - frontend  # Overlay Network
    volumes:
      - web_data:/usr/share/nginx/html   # Mount volume into nginx content directory
    deploy:
      replicas: 2  # Define Replicas
      resources:
        limits:   # Resource Limits for Our container
          cpus: "0.5"
          memory: "256M"
      restart_policy:  # Define Restart Policy If Our Container Is not Starting as Expected
        condition: on-failure

  app:  # App tier Defination
    image: myapp:1.0   # Image name for the app tier
    networks:          # Network Communication
      - frontend
      - backend
    volumes:           # Volume Mounts Section
      - app_logs:/var/log/myapp          # Persist application logs
    deploy:
      replicas: 3
      resources:
        limits:
          cpus: "1.0"
          memory: "512M"
      restart_policy:
        condition: on-failure

  db:            # Defination Of the Data Base Tier
    image: mysql:8.0  # mysql Image Defination
    environment:    # Defining the Environment Variables Related to Initilization
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: mydb
      MYSQL_USER: myuser
      MYSQL_PASSWORD: mypass
    networks:  # Network Section
      - backend
    volumes:    # Volume Mounts Section
      - db_data:/var/lib/mysql           # Persist database Mount Point
    deploy:
      replicas: 1
      resources:
        limits:
          cpus: "1.0"
          memory: "1G"
      restart_policy:
        condition: any

# Define named volumes
volumes:
  web_data:
  app_logs:
  db_data:

# Define overlay networks (needed for Swarm)
networks:
  frontend:
    driver: overlay
  backend:
    driver: overlay
```


