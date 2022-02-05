Containers:

	• Basics of cloud native dev
	• convenient package to ship things
	• Portable, stackable, isolated, lightweight
	• Open specification
	• A container is just a process bound by LINUX primitives (chroot, cgroups., namespaces, netlink,.. )
Develop, Assemble & ship, Deploy & Run

Advantages of Docker:
    
    • Reproducibility 
    • ….

Diff b/w docker & k8s:

	* K8s is orchestration on top of docker
	

Diff b/w VM & Docker/containers:

	• No OS
	• Light weight , …


K8s:

	• Manages workload, monitor apps/health checks
	• Service discovery, rescheduling 

Docker Images:

	• filesystem snapshot that function as the root filesystem of a container at startup + some metadata

Docker hub:

	• Repo/registry for docker images
	

Lifecycle of a container:

	• By default :
		○ All layers of an image are ready-only
	• docker create - creates writable layer
	• Docker start - activates writable layer
	• Docker run -> does both create and start 
	• Docker stop and docker start reuses the writable layer
	• Docker rm deletes the writable layer


Diff b/w image & container:

	• Container is an runtime/instance of image
	• Multiple containers can point to a single image
	• Share images, not containers


Flow of cmds docker run / pull / build:

	• Client -> Docker host <-> dicker hub
    • Client talks to docker_host via socket connection



It is possible to build using dockerd and run using containerd

-> standards -> OCI specs


![This is an image](https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Docker/images/docker_networking.png)
