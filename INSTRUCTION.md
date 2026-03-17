# Docker instructions

## Docker Hub image

Replace `<your_dockerhub_username>` with your Docker Hub username.

- Repository: `docker.io/<your_dockerhub_username>/todoapp`
- Tag: `1.0.0`

## Build

From the project root:

```bash
docker build --build-arg PYTHON_VERSION=3.12-slim -t todoapp .
```

## Run

```bash
docker run --rm -p 8080:8080 todoapp
```

## Open in browser

Open `http://localhost:8080/`.

API is available at `http://localhost:8080/api/`.

## Tag and push to Docker Hub

```bash
docker tag todoapp <your_dockerhub_username>/todoapp:1.0.0
docker push <your_dockerhub_username>/todoapp:1.0.0
```

