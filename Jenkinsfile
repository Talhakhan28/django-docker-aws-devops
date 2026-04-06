pipeline {

    agent { label 'talha' }

    stages {

        stage("Code") {
            steps {
                echo "this is cloning the code"
                git url: "https://github.com/Talhakhan28/django-docker-aws-devops.git", branch: "main"
            }
        }

        stage("Build") {
            steps {
                echo "this is building the code"
                sh "docker build -t notes-app:latest ."
            }
        }

        stage("Push to Docker Hub") {
            steps {
                echo "this is pushing the image to docker hub"
                
                withCredentials([usernamePassword(
                    credentialsId: "dockerHubCred",
                    usernameVariable: "dockerHubUser",
                    passwordVariable: "dockerHubPass"
                )]) {

                    sh "docker login -u ${dockerHubUser} -p ${dockerHubPass}"
                    sh "docker image tag notes-app:latest ${dockerHubUser}/notes-app:latest"
                    sh "docker push ${dockerHubUser}/notes-app:latest"

                }
            }
        }

        stage("Deploy") {
            steps {
                echo "this is deploying the code"
                sh "docker-compose down"
                sh "docker-compose up -d"
            }
        }

    }
}
