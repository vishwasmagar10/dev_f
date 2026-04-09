# DevOps Flask CI/CD Pipeline 🚀

## 📌 Overview

This project demonstrates an end-to-end DevOps pipeline using a Flask application.

## 🧰 Tech Stack

* Python (Flask)
* Docker
* Jenkins (CI/CD)

## 🔄 CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline triggers automatically
3. Application is built and tested
4. Docker image is created
5. Container is deployed

## 🐳 Docker Usage

Build image:

```
docker build -t flask-app .
```

Run container:

```
docker run -p 5000:5000 flask-app
```

## 📂 Project Structure

* app.py → Flask application
* requirements.txt → Dependencies
* Dockerfile → Container setup
* Jenkinsfile → CI/CD pipeline


## 👨‍💻 Author

Vishwas Magar
