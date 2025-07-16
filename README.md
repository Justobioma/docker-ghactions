# 🚀 Node.js CI/CD with Docker

[![Build and Push](https://github.com/justobioma/node-ci-cd-app/actions/workflows/docker.yml/badge.svg)](https://github.com/justobioma/node-ci-cd-app/actions/workflows/docker.yml)

A simple Node.js web app powered by Express, Docker, and GitHub Actions. Every push to the main branch triggers a CI/CD pipeline that builds a Docker image and deploys it to [DockerHub](https://hub.docker.com/repository/docker/justobioma/node-ci-cd-app).

---

## 🧰 Tech Stack

| Tool             | Version     | Purpose                     |
|------------------|-------------|-----------------------------|
| Node.js          | 18.x        | Backend Runtime             |
| Express          | latest      | Web Framework               |
| Docker           | latest      | Containerization            |
| GitHub Actions   | latest      | CI/CD Automation            |

---

## 📦 Project Structure
node-ci-cd-app/ ├── app.js ├── package.json ├── Dockerfile ├── .dockerignore └── .github/ └── workflows/ └── docker.ym

---

## 📡 How It Works

- ✅ Push to `master` triggers GitHub Actions
- 🐳 Builds Docker image using `Dockerfile`
- 🔐 Authenticates securely with DockerHub
- 📤 Pushes image to `justobioma/node-ci-cd-app:latest`

---

## 🛠️ Local Development

Install dependencies:

```bash
npm install

Run the server locally:
node app.js
Visit http://localhost:3000

---

🐳 Build and Run with Docker
To build and run locally:
docker build -t node-ci-cd-app .
docker run -p 3000:3000 node-ci-cd-app

---
🔐 GitHub Secrets Required
| Name | Description | 
| DOCKER_USERNAME | Your DockerHub username | 
| DOCKER_PASSWORD | Your DockerHub password/token | 

Add these under Repo → Settings → Secrets → Actions

---
🧪 Test the Pipeline
Make any change and push:
git commit -am "Trigger build"
git push origin master

Check the Action tab for status







