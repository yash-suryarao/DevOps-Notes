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

__1. Image Commands:__
* __docker pull image_name:tag :__ Pull an image from a registry (Docker hub).
```console
#Example

> docker pull nginx:latest
```

* __docker build -t image_name path-to-dockerfile :__ Build an image from a Dockerfile.
```console
#Example

> docker build -t myapp .
```

* __docker push image_name:tag :__
```console
#Example

> docker push myapp:v1
```

* __docker images :__ List all images on the local machine
```console
#Example

> docker images
```

* __docker image inspect image_name:tag :__ Inspect details of an image.
```console
#Example

> docker images inspect myapp:v1
```

* __docker save -o image_name.tar image_name:tag :__ Save an image to a tar archive
```console
#Example

> docker save -o myapp.tar myapp:v1
```


* __docker rmi image_name:tag :__ Remove an image
* __docker rm [image_name/image_id]__
```console
#Example

> docker rmi myapp

OR

> docker rm fd48f19954f
```

* __Tag  an Image:__ Tags an image with a different name, providing a way to reference the same image under different names.
```console
#Example

> docker tag myapp:latest myapp:v1
```

* __Remove Ununsed Images:__ Remove all dangling (unused) images.
```console
#Example

> docker image prune
```

* __Remove All images:__ Removes all images on the local machine.
```console
#Example

> docker rmi $(docker image -q)
```


__2. Container Commands:__
* __docker run:__ Run a container from an image.
```console
#Example

> docker run -d -p 8080:80 myapp:v1
```

* __docker ps:__ List all running containers.
```console
#Example

> docker ps
```
* __docker ps -a:__ List all containers (incliding stopeed ones).
```console
#Example

> docker ps -a
```

* __docker stop:__ Stop a running container.
```console
#Example

> docker stop container_name_or_id
```

* __docker start:__ Start a stopped container:
```console
#Example

> docker docker start container_name_or_id
```

* __docker run -it:__ Run container in interactive mode:
```console
#Example

> docker run -it container_name_or_id
```

* __docker run -it name sh:__ Run container in interactive shell mode:
```console
#Example

> docker run -it container_name_or_id sh
```

* __docker rm:__ Remove stopped container.
* __docker rm -f :__ Remove a running container (forcefully).
```console
#Example

> docker rm container_name_or_id

OR

> docker rm -f container_name_or_id
```

* __dokcer inspect:__ Inspect details of a container.
```console
#Example

> docker inspect container_name_or_id
```

* __docker exec:__ Execute a command in a running container.
```console
#Example

> docker exec -it container_id bash
```

* __docker logs:__ View logs of a container.
```console
#Example

> docker logs container_id
```

