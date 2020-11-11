# Creating a Production-Grade React App Workflow

## Docker commands

- Build development Dockerfile:

  ```bash
  docker build -f Dockerfile.dev .
  ```

- Run the container:

  - Normal method:

    ```bash
    docker run -it -p 3000:3000 <CONTAINER_ID>
    ```

  - Using docker volume (Will reflect our local files changes) :

    ```bash
    docker run -it -p 3000:3000 -v /app/node_modules -v $(pwd):/app <image_id>
    ```

  - Using docker-compose:

    ```bash
    docker-compose up
    ```

## Available Scripts

In the project directory, you can run:

- `yarn start`

- `yarn test`

- `yarn build`

- `yarn eject`
