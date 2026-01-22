# Node.js Docker Example

This is a simple Node.js app for Docker, based on the official Docker tutorial.

## How to use

1. **Build the Docker image locally:**
   ```sh
   docker build -t docker-node-app ./app
   ```
2. **Run the app:**
   ```sh
   docker run -p 3000:3000 docker-node-app
   ```
3. **Visit** [http://localhost:3000](http://localhost:3000)

## CI/CD

- On every push to `main` (or changes in `app/`), GitHub Actions will build and publish the Docker image to GitHub Packages (ghcr.io).

## Files
- `app/server.js`: Node.js app
- `app/package.json`: Node.js dependencies
- `app/Dockerfile`: Docker build instructions
- `.github/workflows/docker-image.yml`: CI/CD pipeline

## Reference
- [Docker tutorial app](https://docs.docker.com/get-started/02_our_app/)
- [GitHub Actions Docker publish](https://docs.github.com/en/actions/publishing-packages/publishing-docker-images)
