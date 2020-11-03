# Section 2: Manipulating Containers with the Docker Client

### Creating and Running a container from an image

```bash
docker run <image name>
```

Ex.

```bash
docker run hello-world
```

### Overriding Default Commands

Ex.

```bash
docker run busybox ls
```

### Listing All Running Containers

```bash
docker ps

docker ps --all
```

### Container Lifecycle

`docker run = docker create + docker start`

```bash
docker create <image name>

docker start -a <container id>
```

### Removing Stopped Containers

```bash
docker system prune
```

### Retrieving Log Outputs

```bash
docker logs <container id>
```

### Stopping Containers

```bash
docker stop <container id>
```

```bash
docker kill <container id>
```

### Executing Additional Commands in Running Containers

```bash
docker exec -it <container id> <command>
```

`exec`: Run another command
`-it`: Allow us to provide input to the container

Ex.

Terminal 1:

```bash
docker run redis
```

Terminal 2:

```bash
docker exec -it <container id> redis-cli
```

### Getting a Command Prompt in a Container

```bash
docker exec -it <container id> sh
```

### Starting with a Shell

```bash
docker run -it <image name> sh
```
