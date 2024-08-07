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
