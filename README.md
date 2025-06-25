Use Python or Node.js
# Dockerize a Python Flask App
Flask App with Python 

**1. 🔧Create Project Files**
app.py

**requirements.txt**
nginx
flask

**2. 🐳Create Dockerfile**
Python Dockerfile
Dockerfile.txt 

**3. ▶️Build & Run**
bash

**Build the image**
docker build -t flask-app.

**Run the container**
docker run --p 5000:5000 flask-app
Then visit: http://localhost:5000

# Dockerize a Node.js Express App

**1. 🔧Create Project Files**
   app.js
   package.json

**2. 🐳Create Dockerfile**
Js Dockerfile

**3. ▶️Build & Run**
**bash**
docker build -t node-app .
docker run -p 3000:3000 node-app

**Then visit: http://localhost:3000**

#  Jenkins with Docker access
**🧰 Step 1: Run Jenkins with Docker Socket Access**
docker run -d \
  --name jenkins \
  -p 8080:8080 -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -u root \
  jenkins/jenkins:lts

**🔁 This command:**
Runs Jenkins as root (so it can run Docker)
Mounts the host Docker socket into the container
Uses jenkins/jenkins:lts image

**🔧 Step 2: Install Docker CLI inside Jenkins Container**
docker exec -u root -it jenkins bash
Then inside the container:
**bash**
apt update
apt install -y docker.io
exit

**Now Jenkins container has access to host Docker daemon and can run** docker build, docker run, etc.




