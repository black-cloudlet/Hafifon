### Subjects Checklist 

*Read the `Docker Deep Dive` Book, and make sure you understand the following subjects:*
- Linux namespaces
- Linux cgroups
- Linux capabilities 
- Docker Engine (runc, containerd)
- Dockerfile 
- Docker Image (COW, image layers)
- Docker network managment 
- Docker storage managment (Drivers and Volumes)
- Docker commands 
  - How can you list all the docker images on your machine?
  - How can you list all the docker containers on your machine?
  - How can you enter a running container? (using bash)
  - What does the `-d` flag do when starting a container?
- Docker Compose 

**Do NOT read the following chapters:
Docker swarm
Deploying apps with docker stacks
WebAssembly**


### Exercise 
- Create the following scenario:
  - Start two WordPress docker containers and one MySQL container (Both WordPress should use the MySQL container as its database)
  - Add an nginx docker container as a load balancer between the two WordPress containers
  - Create a docker-compose file for creating the scenario

### Read
- Docker's [Get Started](https://docs.docker.com/get-started/)
- [Docker docs site](https://docs.docker.com/storage/)


