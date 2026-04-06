# Django Docker AWS CI/CD Deployment

This project demonstrates how to deploy a Django application using Docker in a production-style environment with a complete CI/CD pipeline. The application is containerized using Docker and automatically deployed on an AWS EC2 instance using Jenkins with a Multi-Agent architecture. The goal of this project is to simulate a real-world DevOps workflow where code changes are automatically built and deployed.

## Tech Stack

Django, Jenkins, Jenkins Multi-Agent Architecture, Docker, Docker Compose, Nginx, Gunicorn, MySQL, AWS EC2, GitHub Webhooks.

## Architecture

Nginx → Gunicorn → Django → MySQL

Nginx acts as a reverse proxy and handles incoming HTTP requests. Gunicorn runs the Django application server and communicates with the Django application. MySQL is used as the database to store application data. Docker Compose manages and orchestrates the multi-container environment including the Django application, database, and Nginx services.

## CI/CD Workflow

GitHub → Webhook → Jenkins Master → Jenkins Agent → Docker Build → Docker Compose → Deploy on AWS

Whenever new code is pushed to the GitHub repository, a webhook automatically triggers Jenkins. The Jenkins master schedules the pipeline and assigns the build task to a Jenkins agent. The agent pulls the latest code, builds the Docker image, and deploys the application using Docker Compose on the AWS EC2 instance. This automation ensures faster and more reliable deployments.

## Project Structure

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

## Run Locally

Clone the repository:

git clone https://github.com/Talhakhan28/django-docker-aws-deployment.git

Navigate to the project directory:

cd django-docker-aws-deployment

Build and start the containers:

docker compose up --build

Access the application in your browser:

http://localhost

## Deployment

The application is deployed on an AWS EC2 instance using Docker containers. Nginx works as the reverse proxy, Gunicorn runs the Django application server, and MySQL is used as the database. Docker Compose manages the containers and networking between services. Jenkins automates the CI/CD pipeline so that every push to GitHub triggers an automatic build and deployment.

## Screenshots

Application Running  
<img width="784" height="625" alt="image" src="https://github.com/user-attachments/assets/8531b902-1203-4179-9255-cef4233d4a3a" />

CI/CD Pipeline  
<img width="891" height="620" alt="image" src="https://github.com/user-attachments/assets/08a9d01d-8c0a-4dc6-b8a4-642f35e1bac7" />

Docker Containers Running  
<img width="1404" height="142" alt="image" src="https://github.com/user-attachments/assets/cba1dce7-bbff-439d-b07f-2b8e0f1a92cd" />

## Author

Talha Khan  
  
DevOps & Cloud Enthusiast
