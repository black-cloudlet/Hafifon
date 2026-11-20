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

*Make sure you understand the following subjects as well (they are not in the book):*
- Podman
  - What is Podman? What are the main differences between Podman and Docker? (Think about daemon, root privileges and pods)
  - What are rootless containers? Why are they important for security?
  - What is a pod in Podman? How is it related to a Kubernetes pod?
  - Can you run Docker commands and Dockerfiles with Podman?
  - How can you run a Podman container as a systemd service? (Read about Quadlet)
- Moving images without a registry
  - What do `docker save` and `docker load` do? When would you need them?
  - What is the difference between `docker save`/`docker load` and `docker export`/`docker import`?
  - Skopeo
    - What is Skopeo? What can it do that `docker pull` and `docker push` can't?
    - Does Skopeo need a running daemon? Why does it matter?
    - What do `skopeo inspect`, `skopeo copy` and `skopeo sync` do?
    - Read about the different Skopeo transports (`docker://`, `docker-archive:`, `oci:`, `dir:`)

**Do NOT read the following chapters:
Docker swarm
Deploying apps with docker stacks
WebAssembly**


### Exercise 
- Create the following scenario:
  - Start two WordPress docker containers and one MySQL container (Both WordPress should use the MySQL container as its database)
  - Add an nginx docker container as a load balancer between the two WordPress containers
  - Create a docker-compose file for creating the scenario
- Podman
  - Run the same scenario with Podman as a non-root user, with all the containers in a single pod
  - Make one of the containers start automatically on boot, as a systemd service
- Moving images
  - Use `docker save` to save all the images of the scenario into a single tar file
  - Copy the tar file to a second machine that has no internet access, use `docker load` and run the scenario there
  - Use `skopeo inspect` to see the tags and layers of the `nginx` image on Docker Hub, without pulling it
  - Run a local registry (using the `registry` image), and use `skopeo copy` to copy the scenario images into it
  - Use `skopeo copy` to copy an image from the local registry into a `docker-archive` tar file, then load it with Podman

### Read
- Docker's [Get Started](https://docs.docker.com/get-started/)
- [Docker docs site](https://docs.docker.com/storage/)
- [Podman docs](https://docs.podman.io/en/latest/)
- [Skopeo GitHub](https://github.com/containers/skopeo)


