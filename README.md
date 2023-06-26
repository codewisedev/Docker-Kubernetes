# Docker and Kubernetes config files

## Stacks List

- APM Server
- KeyCloak
- RabbitMQ
- Redis

## Some Commands

### Docker

#### Docker Management Commands

- `docker version` Shows the Docker CLI and server versions.
- `docker info` Displays system-wide information about the Docker installation.
- `docker run` Runs a command in a new container.
- `docker start` Starts one or more stopped containers.
- `docker stop` Stops one or more running containers.
- `docker restart` Restarts one or more containers.
- `docker pause` Pauses one or more running containers.
- `docker unpause` Unpauses one or more paused containers.
- `docker kill` Sends a SIGKILL to one or more running containers.
- `docker rm` Removes one or more containers.
- `docker ps` Lists the containers that are currently running.
- `docker inspect` Shows information about a container.
- `docker logs` Gets logs from a container.
- `docker events` Gets real-time events from the server.
- `docker wait` Blocks until one or more containers stop.
- `docker update` Updates the configuration of one or more containers.

#### Docker Image Commands

- `docker images` Lists all images that are locally stored on the host machine.
- `docker pull` Pulls an image from a registry.
- `docker push` Pushes an image to a registry.
- `docker rmi` Removes one or more images.
- `docker build` Builds an image from a Dockerfile.

#### Docker Registry Commands

- `docker login` Logs in to a registry.
- `docker logout` Logs out from a registry.
- `docker search` Searches the Docker Hub for images.

#### Docker Network Commands

- `docker network create` Creates a new network.
- `docker network ls` Lists all networks.
- `docker network inspect` Shows information about a network.
- `docker network connect` Connects a container to a network.
- `docker network disconnect` Disconnects a container from a network.

#### Docker Volume Commands

- `docker volume create` Creates a new volume.
- `docker volume ls` Lists all volumes.
- `docker volume inspect` Shows information about a volume.
- `docker volume rm` Removes one or more volumes.

### Kubernetes

- `kubectl` The main command-line tool for interacting with Kubernetes clusters.
- `kubectl apply` Creates or updates a resource in a Kubernetes cluster based on the configuration file provided.
- `kubectl create` Creates a new Kubernetes resource from a configuration file or command-line arguments.
- `kubectl delete` Deletes one or more resources from a Kubernetes cluster.
- `kubectl describe` Displays detailed information about a Kubernetes resource.
- `kubectl edit` Edits the configuration of a Kubernetes resource in real-time.
- `kubectl exec` Runs a command inside a container running in a Pod.
- `kubectl get` Displays information about one or more Kubernetes resources.
- `kubectl logs` Displays the logs for a specific container within a Pod.
- `kubectl port-forward` Forwards network traffic from a local host to a container running in a Pod.
- `kubectl rollout` Performs a rollout of an update to a Deployment or DaemonSet.
- `kubectl scale` Scales the number of replicas in a Deployment or ReplicaSet.
- `kubectl set` Changes the value of one or more fields in a Kubernetes resource.
- `kubectl top` Displays resource usage metrics for nodes and pods.
- `kubectl version` Displays the version of kubectl and the Kubernetes API server.
