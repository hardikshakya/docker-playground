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
