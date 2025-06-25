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
bash
docker build -t node-app .
docker run -p 3000:3000 node-app

**Then visit: http://localhost:3000**





