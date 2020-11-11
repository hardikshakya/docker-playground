# All Projects Related Docs

## Container Port Mapping

```bash
docker run -p <route incoming requests to this port on localhost to...> : <...this port inside the container> <image id/name>
```

Ex.

```bash
docker run -p 5000:8080 hardikshakya/simplenodeweb
```

## Automatic Container Restarts

- In docker-compose file:

  ```bash
  restart: <key>
  ```

| Key            | Action                                                                |
| -------------- | --------------------------------------------------------------------- |
| 'no'           | Never attempt to restart this container if it stops or crashes        |
| always         | If this container stops "for any reason" always attempt to restart it |
| on-failure     | Only restart if the container stops with an error code                |
| unless-stopped | Always restart unless we (the developers) forceibly stop it           |

## Docker Volumes

- Here we setting up a mapping from the folder inside the container to a folder out side of th e container.
- It will reflect our local files changes to container without re-building the container.

```bash
docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>
```

- `-v /app/node_modules`: Put a bookmark on the node_modules folder
- `-v $(pwd):/app`: Map the pwd into the /app folder
