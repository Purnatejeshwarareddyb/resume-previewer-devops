pipeline {

    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Purnatejeshwarareddyb/resume-previewer-devops.git'
            }
        }

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
pipeline {

    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Purnatejeshwarareddyb/resume-previewer-devops.git'
            }
        }

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
            echo 'CI/CD Pipeline Success 🚀'
        }

        failure {
            echo 'Pipeline Failed ❌'
        }

    }
}
