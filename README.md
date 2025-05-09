# Python Flask - Demo Web Application

This is a simple Python Flask web application. The app provides system information and a realtime monitoring screen with dials showing CPU, memory, IO and process information.

The app has been designed with cloud native demos & containers in mind, in order to provide a real working application for deployment, something more than "hello-world" but with the minimum of pre-reqs. It is not intended as a complete example of a fully functioning architecture or complex software design.

Typical uses would be deployment to Kubernetes, demos of Docker, CI/CD (build pipelines are provided), deployment to cloud (Azure) monitoring, auto-scaling

## Screenshot

![screen](https://user-images.githubusercontent.com/14982936/30533171-db17fccc-9c4f-11e7-8862-eb8c148fedea.png)

## 🍕 Prerequisites

- 🐳 **Docker** (build & run containers)  
- 🦊 **GitLab** account (CI/CD magic)  
- 📦 **Docker Hub** account (store your images)  

## 📂 Repo Structure

.gitlab-ci.yml # CI pipeline (test & build)
build/ # Dockerfile + build scripts
src/ # Your awesome app code
tests/ # Unit & integration tests
Makefile # Shortcut commands (build, test, push, run)

## 🚀 Quick Start

```bash
git clone https://github.com/DUCK8-bit/DevOps.git
cd DevOps

# 🔨 Local build & run
docker build -t duck8bit/python-demoapp .
docker run -p 5000:5000 duck8bit/python-demoapp

# 🧪 Tests
make test

# 📤 Push to Docker Hub (set $REGISTRY_USER & $REGISTRY_PASS)
make push

#🤖 GitLab CI
Our pipeline does the heavy lifting for you:

#🧪 test – Sets up Python, installs dependencies, and runs tests.

#🐳 build – Builds, tags, and pushes your Docker image to Docker Hub.

Triggers on every push to main and on merge requests.
Check CI/CD > Pipelines in GitLab to see the action! ✨

#🌐 Deployment
Live and kicking on Render (auto-updates on new image):

➡️ https://devops-12.onrender.com

#🤝 Contributing
#🍴 Fork it

🌿 Create your feature branch: git checkout -b feature/xyz

📝 Commit your changes: git commit -m 'Add new feature'

🌍 Push to GitLab: git push origin feature/xyz

🔃 Open a Merge Request

#📜 License
 MIT © DUCK8-bit. Enjoy! 🥳
