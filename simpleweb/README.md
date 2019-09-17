# Building the container image
docker build -t [docker-hub-id]/[image-name]:latest|prod|dev .

# Starting the container
docker run -p 4100:8080 [docker-hub-id]/[image-name]

# Getting inside the container's bash at start (This overrides the default start up command)
docker run -it [docker-hub-id]/[image-name] sh

# Getting inside the container's bash while it's alive
docker exec -it [container-id] sh