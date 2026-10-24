# WARHOG

A simple WARHOG landing page served by Nginx.

## Run locally with Docker Compose

From the repository directory, run:

```sh
docker compose up --build
```

Open [http://localhost:8080](http://localhost:8080) to view the page. Stop the service with `Ctrl+C`, or run `docker compose down` in another terminal.

## Build and publish the image

The GitHub Actions workflow in `.github/workflows/deploy.yml` builds and publishes the image to Docker Hub whenever a commit is pushed to `main`.

In the repository's **Settings → Secrets and variables → Actions**, add these repository secrets:

- `DOCKERHUB_USERNAME` — your Docker Hub username
- `DOCKERHUB_TOKEN` — a Docker Hub access token with permission to push images

The workflow publishes the image as `DOCKERHUB_USERNAME/warhogweb2026:latest`.
