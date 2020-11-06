# Docker Compose

- Separate CLI that gets installed along with Docker
- Used to start up multiple Docker containers at the same time
- Automates some of the long-winded arguments we were passing to like 'docker run'

## Commands

- Buils + run:

  ```bash
  docker-compose up --build
  ```

- Launch in background:

  ```bash
  docker-compose up -d
  ```

- Stop containers:

  ```bash
  docker-compose down
  ```

- Container Status with Docker Compose:

  ```bash
  docker-compose ps
  ```
