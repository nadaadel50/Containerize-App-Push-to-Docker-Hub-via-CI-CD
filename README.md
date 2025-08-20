
## 🐳 Docker Support

This project is fully containerized. You can **build, run, and deploy** it easily using Docker.

### 🔧 Prerequisites

- [Docker](https://www.docker.com/get-started) installed locally  
- Docker Hub account (for pulling/pushing images)  

---

### 🏗️ Build & Run Locally

1. **Build the Docker image**

```bash
docker build -t <your-dockerhub-username>/app:latest .

    Run the container

docker run -p 3000:3000 <your-dockerhub-username>/app:latest

    Test the app

Open your browser at:
👉 http://localhost:3000

    ⚠️ Change 3000 if your app runs on a different port.

📥 Pull & Run from Docker Hub

    Pull the latest image

docker pull <your-dockerhub-username>/app:latest

    Run it

docker run -p 3000:3000 <your-dockerhub-username>/app:latest

    Run a specific version

docker run -p 3000:3000 <your-dockerhub-username>/app:1.0.0

⚡ CI/CD with GitHub Actions

This repository uses GitHub Actions to build and publish the Docker image automatically.

    ✅ Runs on push to main branch

    ✅ Builds Docker image

    ✅ Tags as latest and version (1.0.0)

    ✅ Pushes to Docker Hub

🔑 Required GitHub Secrets

    DOCKERHUB_USERNAME → Your Docker Hub username

    DOCKERHUB_TOKEN → Docker Hub access token

Workflow file: .github/workflows/docker.yaml

