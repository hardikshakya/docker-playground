# Section 3: Building Custom Images Through Docker Server

## Building a Dockerfile

- First create `Dockerfile`

```Dockerfile
# Use an existing docker image as a base
FROM alpine

# Download and install a dependency
RUN apk add --update gcc
RUN apk add --update redis

# Tell the image what to do when it starts
# as a container
CMD ["redis-server"]
```

- Now create build

```bash
docker build .
```

- Run it

```bash
docker run <image id>
```

## Tagging an Image

```bash
docker build -t <your_docker_id + / + repo-project_name + : version> .
```

Ex.

```bash
docker build -t hardikshakya/redis-image:latest .

docker run hardikshakya/redis-image
```
