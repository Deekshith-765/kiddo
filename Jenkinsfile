pipeline {
    agent any

    environment {
        USERNAME = 'vijin'
        IMAGE = "zoople-devops-workshop-${USERNAME}"
        DOMAIN = "${USERNAME}.workshop.zoople.in"
    }

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh "docker build -t $IMAGE:latest ."
                }
            }
        }
    }
}