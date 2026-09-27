# Demo App — Spring Boot + GitHub Actions + Docker Hub

See the walkthrough in the chat for full details. Quick reference:

1. Push this folder to a new GitHub repo.
2. In GitHub repo Settings → Secrets and variables → Actions, add:
   - `DOCKER_USERNAME` — your Docker Hub username
   - `DOCKER_PASSWORD` — a Docker Hub access token (not your real password)
3. Push to `main`. The workflow in `.github/workflows/ci-cd.yml` builds the app,
   builds a Docker image, and pushes it to Docker Hub automatically.
4. Run locally: `docker run -p 8080:8080 <your-dockerhub-username>/demo-app:latest`
5. Visit `http://localhost:8080/` — you should see the hello message.
