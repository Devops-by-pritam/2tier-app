```markdown
 🏗️ 2-Tier Microservices App on OpenShift

This project demonstrates a simple 2-tier architecture composed of:
- A frontend microservice (UI)
- A backend microservice (API)

Both services are containerized and deployed on Red Hat OpenShift using Kubernetes manifests.
---

 🚀 Deployment Steps (on OpenShift)

> Prerequisites:
> - Access to OpenShift cluster (like [OpenShift Sandbox](https://developers.redhat.com/developer-sandbox))
> - `oc` CLI installed and configured
> - DockerHub account or image registry access

 1. Clone the repository

```bash
git clone https://github.com/Devops-by-pritam/2tier-app.git
cd 2tier-app
````

 2. Build and Push Docker Images

```bash
 Example for backend
cd backend
docker build -t <dockerhub-user>/backend:latest .
docker push <dockerhub-user>/backend:latest

 Example for frontend
cd ../frontend
docker build -t <dockerhub-user>/frontend:latest .
docker push <dockerhub-user>/frontend:latest
```

 3. Deploy to OpenShift

```bash
 Log in to your OpenShift cluster
oc login ...

# Apply Kubernetes manifests
cd ../k8s
oc apply -f backend-deployment.yaml
oc apply -f backend-service.yaml
oc apply -f frontend-deployment.yaml
oc apply -f frontend-service.yaml
```

 4. Expose Route (if needed)

```bash
oc expose service frontend
```

Then access the frontend app via the generated OpenShift route.

---

 🔧 Tech Stack

* Frontend: HTML/CSS/JS or React (customizable)
* Backend: Node.js / Python / Go (check `/backend`)
* Platform: OpenShift (Kubernetes)
* CI/CD: Manual or GitHub Actions (optional)

---

 🙌 Contributions Welcome

Feel free to fork, explore, and contribute!

1. 🍴 Fork this repo
2. 🛠️ Make your changes
3. 🔁 Submit a Pull Request

---

 📬 Maintainer

* **Pritam Mane** | [GitHub](https://github.com/prritam) | [X](https://x.com/priitam03) | [Blog](https://medium.com/@pritammane7666)

---
```

