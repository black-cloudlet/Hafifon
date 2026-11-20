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


### Read
- Docker's [Get Started](https://docs.docker.com/get-started/)
- [Docker docs site](https://docs.docker.com/storage/)
- [Podman docs](https://docs.podman.io/en/latest/)
- [Skopeo GitHub](https://github.com/containers/skopeo)


