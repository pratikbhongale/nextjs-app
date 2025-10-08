# Containerize an application using Docker, Github Actions and Minikube

This project demonstrates:

- Dockerizing a Next.js app
- Pushing the image to GitHub Container Registry (GHCR) using GitHub Actions
- Deploying the app to Kubernetes with Minikube

---

## 🔧 Local Development

```bash
cd app
npm install
npm run dev

## 📁 Project Structure

.
├── app/ 
├── k8s/
│ ├── deployment.yaml 
│ └── service.yaml
├── Dockerfile
├── .dockerignore
├── .github/
│ └── workflows/
│ └── docker-build.yml 
└── README.md

#Prerequisites
- npm & nodejs
- docker
- kubectl
- Minikube
- Github Account

🐳 Run with Docker
docker build -t nextjs-app .
docker run -p 3000:3000 nextjs-app

☸️ Deploy to Minikube
minikube start
kubectl apply -f k8s/
minikube service nextjs-service
It will automatically start your service in default browser or visit http://<minikube-ip>:targetPort 

