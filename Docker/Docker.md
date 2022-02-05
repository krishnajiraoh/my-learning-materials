# Containers:

	• Basics of cloud native dev
	• convenient package to ship things
	• Portable, stackable, isolated, lightweight
	• Open specification
	• A container is just a process bound by LINUX primitives (chroot, cgroups., namespaces, netlink,.. )
    • Develop, Assemble & ship, Deploy & Run

# Advantages of Docker:
    
    • Reproducibility 
    • ….

# K8s:

	• Manages workload, monitor apps/health checks
	• Service discovery, rescheduling 

# Docker Images:

	• filesystem snapshot that function as the root filesystem of a container at startup + some metadata

# Docker hub:

	• Repo/registry for docker images
	

# Lifecycle of a container:

	• By default :
		○ All layers of an image are ready-only
	• docker create - creates writable layer
	• Docker start - activates writable layer
	• Docker run -> does both create and start 
	• Docker stop and docker start reuses the writable layer
	• Docker rm deletes the writable layer

# Diff b/w docker & k8s:

	* K8s is orchestration on top of docker
	

# Diff b/w VM & Docker/containers:

	• No OS
	• Light weight , …
	
# Diff b/w image & container:

	• Container is an runtime/instance of image
	• Multiple containers can point to a single image
	• Share images, not containers


# Flow of cmds docker run / pull / build:

	• Client -> Docker host <-> dicker hub
    • Client talks to docker_host via socket connection


# Advantages of Layers:

	• Reuse of layers
    • Only delta is downloaded



It is possible to build using dockerd and run using containerd

-> standards -> OCI specs


# Docker Networking:

    • NAT 
![Docker Networking](https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Docker/images/docker_networking.png)


# Volumes:

    • Why?
		○ Writable layer lost once removed 
	• Get data from host file system

![Docker Volumes](https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Docker/images/docker_volumes.png)
    In Named volume, the data will be encrypted in the destination

# Dockerfile:

• explains ow the image must build
• each line is a layer in the image

    • FROM
        • Scratch or base image
        • Ex: FROM debian:jessie
        • Ex: FROM SCRATCJ
    • ENV
        • Env variable
        • Ex: ENV htttp_proxy http://proxy:8080
    • LABEL
        • Sets meta-data of image, key-value pairs
        • Ex: LABEL key="value"
    • COPY
        • Copy from build-context/hard disk to image
        • Does not copy inside the image
        • Ex: copy default.conf /etc.nginx/conf.d/
    • ADD
        • Can be from URL or extract from tar/jar etc
    • RUN
        • Runs specific cmd in image
    • EXPOSE
        • Expose a port / also automatically
    • CMD
        • Run the cmd after building the image
        • If multiple, only the last will be executed 
        • Can be overridden by container instantiation (from docker args)
    • ENTRYPOINT
        • Sets the program to run after instantiation 
    • USER
        • Set the active user
        • If none, will run commands as root & cause security issues on the host
            ○ Hacker can gain root privileges 


# MultiStage build
![Docker Multistage build](https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Docker/images/docker_multistage.png)

## Commands
### Getting Started:

    • docker pull <image>
    • docker pull <image>:<tag> --> to pull a specify layer
    • docker container list -a
    • docker rm -f <id> -- forcefully terminate even if running
    • docker run -p <host port>:<container port>
        ○ Specify port number
    • docker run -P 
        ○ Random porting
    • docker inspect <container_id>

### Binding:

	• Bind : docker run -it --mount type=bind, source=/home/vagrant,target=/mnt/home alpine:3.8
	• Named : docker run -d -P --mount source=jenkins_home,target=/var/jenkins_home jenkins/jenkins:lts
		○ Named volume : jenkins_home
	• docker volume inspect <volume_name>

### History:

	• docker image history <image>

### Tag:

	• docker tag <image> <image>:<tag>
	• docker tag <image_id> <repo_url> /<name>:<version>

### Debugging:

    • Interactive mode in docker run -i -t
	    - Debug, troubleshoot in a terminal
	    - Both stdin and stdout open
	    - For ex: docker run -I -t <image> /bin/sh -> terminal of image

### Run in background

    • Docker run -d unbuntu
	• Alive without stdin open


# To Read:

    • CMD: commit vs tag , Docker login, Registry
