## What is Docker?
Docker is __Containerization__ PaaS tool (container runtime engine) to create, run & deploy applications in containers.

## What is Docker Container?
Docker Container is __lightweight__ pckage of code, libraries, & dependencies required for an application to run and containers are isolated from one another.

<img height=250 width=400 src="https://github.com/user-attachments/assets/4fa64b69-8da0-4c89-ac35-bb09217ca0c7"> <br>

Docker applications run in containers that can be used on any system: a developer’s laptop, systems on premises, or in the cloud. (it runs the same)
Containers share the host operating system's kernel, but they have their own isolated file system, processes, and networking.

## Difference between Virtual Machines and Containers

![image](https://github.com/user-attachments/assets/5d3c38b9-05af-4930-bd1e-3ef1b7ad3465)

<table>
  <tr>
    <th> Virtual Machines </th>
    <th> Containers </th>
  </th>
  <tr>
    <td>  </td>
    <td>  </td>
  </tr>
  <tr>
    <td>  </td>
    <td>  </td>
  </tr>
  <tr>
    <td>  </td>
    <td>  </td>
  </tr>
</table>

## Advantages of Containerization over traditional deployment methods
### Advantages:
* Consistent test environment for development and QA.
* Cross-platform packages called images.
* Isolation and encapsulation of application dependencies.
* Ability to scale efficiently, easily, and in real time.
* Enhances efficiency via easy reuse of images.

### Disadvantage:
* Compatibility issue: Windows container won’t run on Linux machines and vice versa


## What is Container Image?
A container image is a read-only, standalone, executable package of software that includes everyting needed to run an application: code, runtime, system tools, system libraries and settings. It's similat to a snapshot in a Virtual Machine, and it's immutable (that can't modified once created). We can duplicate, share or delete it or build a new image on top of it. 

## Docker Architecture

![image](https://github.com/user-attachments/assets/53307fa8-3875-43bb-8027-a63a26193b08)

Docker uses a __client-server architecture__ to manage and run containers. The __Docker client__ talks to the __Docker daemon__, which does the heavy lifting od buiding, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or we can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. Another Docker client is Docker Compose, that lets you work with applications consisting of a set of containers.

### 1. Docker Client:
* The Docker client (docker) is a command-line interface (CLI) or (GUI) that allows users to interact with Docker. It's used to manage Docker containers, images, networks, volumes, and other Docker objects. The Docker client can communicate with more than one daemon.
* It sends commands to the Docker daemon to perform various tasks.

### 2. Docker Daemon:
* The Docker daemon is a background process that manages Docker containers on a host system.
* It listens for Docker API requests and takes care of building, running, and managing containers

### 3. Docker Registry:
* Docker images can be stored and shared through Docker registries.
* A Docker registry is a repository for Docker images, and it can be public (like Docker Hub) or private.

### 4. Docker Hub:
* Docker Hub is a cloud-based registry service provided by Docker, where users can find, share, and store Docker images.
* It serves as a central repository for Docker images. 




##  Docker Commands

__1. IMAGE COMMAND:__

* __docker login:__ Login with docker account.
```console
# Example
docker login -u [user-name] -p [password]
```

* __docker build:__ Build an image from a Dockerfile.
```console
# Command
docker build -t <image_name> <path_to_dockerfile>

OR

# Build and image from a Dockerfile without the cache
docker build -t <image_name> . -no-cache 

# Example
docker build -t myapp .
```

* __docker pull:__ Pull an image from a registry (Docker hub).
```console
# Command
docker pull <image_name>:<tag>

# Example
docker pull nginx:latest
```

* __docker push:__ Push an image to Docker Hub.
```console
# Command
docker push <image_name:tag>

# Example
docker push myapp:v1
```

* __docker images:__ List all images on the local machine
```console
# Example
docker images OR docker image ls
```

* __docker image inspect:__ Inspect details of an image.
```console
# Command
docker image inspect <image_name:tag> 

# Example
docker images inspect myapp:v1
```

* __docker save -o image_name.tar image_name:tag :__ Save an image to a tar archive
```console
# Example
docker save -o myapp.tar myapp:v1
```


* __docker rmi:__ Remove an image
* __docker rm:__ Remove an image or stopped container 
```console
# Command
docker rmi <image_name>:<tag>
OR
docker rm <container_id>

# Example
docker rmi myapp
OR
docker rm fd48f19954f
```

* __Remove All images:__ Removes all images on the local machine.
```console
# Example
docker rmi $(docker image -q)
```

* __Tag  an image:__ Tags an image with a different name, providing a way to reference the same image under different names.
```console
docker tag <source_image>:<tag> <new_image>:<tag>

# Example
docker tag myapp:latest myapp:v1
```

* __Remove Ununsed Images:__ Remove all dangling (unused) images.
```console
# Example
docker image prune
```




__2. CONTAINER COMMAND:__

* __docker run:__ Run a container from an image.
```console
-d : Run container in background
-p : Assign an port

# Example
docker run -d -p 8080:80 myapp:v1

OR

# Run a nammed container from an image:
docker run --name <container_name> <image_name:tag>
```

* __docker ps:__ List all running containers.
```console
# Example
docker ps
```
* __docker ps -a:__ List all containers (incliding stopeed ones).
```console
# Example
docker ps -a
```

* __docker stop:__ Stop a running container.
```console
# Example
docker stop container_name_or_id
```

* __docker start:__ Start a stopped container:
```console
# Example
docker docker start container_name_or_id
```

* __docker run -it:__ Run container in interactive mode:
```console
# Example
docker run -it container_name_or_id
```

* __docker run -it name sh:__ Run container in interactive shell mode:
```console
# Example
docker run -it container_name_or_id sh
```

* __docker rm:__ Remove stopped container.
* __docker rm -f :__ Remove a running container (forcefully).
```console
# Example

docker rm container_name_or_id

OR

docker rm -f container_name_or_id
```

* __dokcer inspect:__ Inspect details of a container.
```console
# Example
docker inspect container_name_or_id
```

* __docker exec:__ Execute a command in a running container.
```console
# Example
docker exec -it container_id bash
```

* __docker logs:__ View logs of a container.
```console
# Example
docker logs container_id
```

* __docker pause:__ Pause a running container.
```console
# Example
docker pause container_name_or_id
```

* __docker unpause:__ Unpause a paused container.

```console
# Example
docker unpause contaoner-namr-or-id
```



## Docker Volumes:
🔗[Ref](https://docs.docker.com/engine/storage/volumes/#choose-the--v-or---mount-flag)

Docker volumes are a way to persist data generated by and used by Docker containers. They provide a mechanism for sharing data between a host machine and Docker containers or between other containers themselves. while [bind mounts](https://docs.docker.com/engine/storage/bind-mounts/) are dependent on the directory structure and OS of the host machine.

A "bind mount" in Docker is a feature that connects a directory on the host computer to a directory in a container. This allows changes made to files in the mounted directory to be reflected in both the host and the container. Bind mounts are stored on the host machine where Docker is running and can be useful for: Saving data between runs, Stateful applications, and Communicating files and directories between the host and the container.

### Types of Volumes:
__1. Named Volumes:__ Named volumes are persistent volumes. Completely managed by Docker, easier to use and manage.

__2. Host Volumes:__ Host Volume maps a directory from the host machine into container.

__3. Anonymous Volumes:__ Similar to named volumes but managed by Docker with a randomly generated name.

Volumes are completely managed by Docker. Volumes have several advantages over bind mounts:
* Volumes are easier to back up or migrate than bind mount.
* we can manage volumes using Docker CLI commands or the Docker Desktop.
* Volumes work on both Linux and Windows containers.
* Volumes can be more safely shared among multiple containers.
* Volume drivers let you store volumes on remote hosts or cloud providers, encrypt the contents of volumes, or add other functionality.
* New volumes can have content pre-populated by a container.
* Volumes on Docker Desktop have much perforamnce than bind mounts from Mac and Windows hosts.


volumes are often a better choice than persisting data in a container's writable layer, because a volume doesn't increase the size of the containers using it, and the volume's contents exist outside the lifecycle of a given container.
If your container generates non-persistent state data, consider using a tmpfs mount to avoid storing the data anywhere permanently, and to increase the container's performance by avoiding writing into the container's writable layer.

* __Docker volume directory in linux: /var/lib/docker/volumes/__


## Volume Commands:
** Only one volume can be mount to single container
** We can't mount volume to running container we should first stop the container then only we can aatach an volume

__1. Create a named volume:__
````console
docker volume create my_volume
````

__2. Mount a volume with '--mount' Flag:__
````console
# Command
docker run -d --name=<container_name> --mount source=<volume_name>,target=<path_in_container> <image_name:tag>

# Example
docker run -d --name=nginx_container --mount source=my_volume,target=/data nginx

# Mount a volume with Specific Permission:
docker run -d --name=nginx_container --mount source=my_volume,target=/data,readonly nginx

# [**In docker volumes are there only Read and Write permission]
````

__3. Mount a volume with '-v' Flag:__
````console
# Command
docker run -d --name=<continer_name> -v <volume_name>:</path-in-container> <image_name>

# Example
docker run -d --name=nginx_container -v my_volume:/data nginx

# Mount a volume with Read-Only Permission:
docker run -d --name=nginx_container -v my_volume:/data:ro nginx
````

__4. Mount a host directory as a volume:__
````console
docker run -v /host/path:/container/path nginx
````

__5. List all volumes:__
````console
docker volume ls
````

__6. Inspect a volume:__
````console
docker volume inspect my_volume
````

__7. Remove a volume:__
````console
docker volume rm my_volume
````

__8. Delete all dangling volumes:__
````console
docker volume prune
````

__9. Remove Container and Associated Volumes:__
````console
docker rm -v [container_name]
````
