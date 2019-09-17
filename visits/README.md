# Running the docker compose images
docker-compose up

# Running the docker compose images but rebuilding the containers
docker-compose up --build

# To run a container in background
docker run -d redis
docker-compose up -d

# All the restart policies in docker compose
"no"
always
on-failure
unless-stopped
eg:
version: '3'
services:
  redis-server:
    image: 'redis'
  node-app:
    restart: "no"
    build: .
    ports:
      - "4001:8081"

# Status of the docker compose containers (should be in the same directory)
docker-compose ps