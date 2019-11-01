# Building the container image
docker build -t [docker-hub-id]/[image-name]:latest|prod|dev .

# Starting the container (lates will be picked by default)
docker run -p 4100:8080 [docker-hub-id]/[image-name]

# Getting inside the container's bash at start (This overrides the default start up command)
docker run -it [docker-hub-id]/[image-name] sh

# Getting inside the container's bash while it's alive
docker exec -it [container-id] sh

# To run the build without the default docker file
docker build -f Dockerfile.dev .

docker run -p 3000:3000 -v $(pwd):/app [container-id]