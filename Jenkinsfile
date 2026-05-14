pipeline {

    agent any

    stages {

        stage('Build Maven Project') {
            steps {
                sh 'cd backend/previewer && mvn clean package'
            }
        }

        stage('Build Docker Containers') {
            steps {
                sh 'docker compose build'
            }
        }

        stage('Deploy Containers') {
            steps {
                sh 'docker compose up -d'
            }
        }

    }

    post {

        success {
            echo 'CI/CD Pipeline Success '
        }

        failure {
            echo 'Pipeline Failed '
        }

    }
}
