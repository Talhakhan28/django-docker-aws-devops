# Django Docker AWS Deployment

This project demonstrates how to deploy a Django application using Docker in a production-style environment. The application is containerized using Docker and deployed on an AWS EC2 instance with Nginx as a reverse proxy and MySQL as the database.

## 🚀 Tech Stack

* Django
* Docker
* Docker Compose
* Nginx
* Gunicorn
* MySQL
* AWS EC2

## 🏗 Architecture

Nginx → Gunicorn → Django → MySQL

* **Nginx** acts as a reverse proxy and handles incoming requests.
* **Gunicorn** runs the Django application server.
* **MySQL** is used as the database.
* **Docker Compose** manages the multi-container setup.

## 📂 Project Structure

```
django-docker-aws-deployment
│
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
├── nginx/
│   └── default.conf
├── notesapp/
├── manage.py
└── README.md
```

## ⚙️ Run Locally

Clone the repository:

git clone https://github.com/Talhakhan28/django-docker-aws-deployment.git

Navigate to the project folder:

cd django-docker-aws-deployment

Build and start the containers:

docker compose up --build

Access the application:

http://localhost

## ☁️ Deployment

The application is deployed on an AWS EC2 instance using Docker containers. Nginx acts as the reverse proxy and Gunicorn runs the Django application server.

## 📸 Screenshots

Add screenshots of:

* Running application in browser
* Docker containers running (`docker ps`)
* AWS EC2 instance dashboard

## 👨‍💻 Author

Talha Khan
BSCS Student | DevOps & Cloud Learner
