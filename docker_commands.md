Docker Commands

docker --version --> Check Docker Version

docker ps --> List Running Containers on the host machine.

docker ps -a --> List All Containers (Including Stopped)

docker images --> Lists docker images on the host machine.

docker build -t <image_name>:<tag> . --> Builds image from Dockerfile.

docker run -d <image_name> --> Runs a Docker container.
    docker run -d -p <host_port>:<container_port> <image_name> 
    docker run -d --name <container_name> -p <host_port>:<container_port> <image_name>
    -d: Run in detached mode.
    --name: Assign a custom name to the container.
    -p: Map host port to container port.
    use docker run --help to look into more arguments.

docker stop <container_id_or_name> --> Stops running container.

docker start <container_id_or_name> --> Starts a stopped container.

docker rm <container_id_or_name> --> Removes a stopped container.

docker rmi <image_id_or_name> --> Removes an image from the host machine.

docker pull <image_name> --> Downloads an image from the configured registry.

docker push --> Uploads an image to the configured registry.

docker exec -it <container_id_or_name> bash --> Executes a command inside a running container

docker network ls --> List Networks

docker network create <network_name> --> Create a Network

docker network connect <network_name> <container_name> --> Adds a container to a specified network.

docker network disconnect <network_name> <container_name> --> Removes a container from a network.

docker volume ls --> Shows all available volumes.

docker volume create <volume_name> --> Creates a new volume.

docker volume inspect <volume_name> --> Displays detailed information about a volume.

docker volume rm <volume_name> --> Deletes a specified volume.

docker inspect <container_or_image_id> --> Provides detailed JSON information about a container or image.

docker logs <container_or_image_id> --> Provides the logs of a specific container