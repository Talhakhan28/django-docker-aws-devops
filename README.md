# Django Docker AWS Deployment

This project demonstrates how to deploy a Django application using Docker in a production-style environment. The application is containerized using Docker and deployed on an AWS EC2 instance with Nginx as a reverse proxy and MySQL as the database.

##  Tech Stack

* Django
* Docker
* Docker Compose
* Nginx
* Gunicorn
* MySQL
* AWS EC2

## Architecture

Nginx → Gunicorn → Django → MySQL

* **Nginx** acts as a reverse proxy and handles incoming requests.
* **Gunicorn** runs the Django application server.
* **MySQL** is used as the database.
* **Docker Compose** manages the multi-container setup.

##  Project Structure

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

##  Run Locally

Clone the repository:

git clone https://github.com/Talhakhan28/django-docker-aws-deployment.git

Navigate to the project folder:

cd django-docker-aws-deployment

Build and start the containers:

docker compose up --build

Access the application:

http://localhost

##  Deployment

The application is deployed on an AWS EC2 instance using Docker containers. Nginx acts as the reverse proxy and Gunicorn runs the Django application server.

##  Screenshots

<img width="784" height="625" alt="image" src="https://github.com/user-attachments/assets/8531b902-1203-4179-9255-cef4233d4a3a" />
<img width="891" height="620" alt="image" src="https://github.com/user-attachments/assets/08a9d01d-8c0a-4dc6-b8a4-642f35e1bac7" />
<img width="1404" height="142" alt="image" src="https://github.com/user-attachments/assets/cba1dce7-bbff-439d-b07f-2b8e0f1a92cd" />




## 👨‍💻 Author

Talha Khan

