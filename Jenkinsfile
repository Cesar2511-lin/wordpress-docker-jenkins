pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Cesar2511-lin/wordpress-docker-jenkins.git'
            }
        }

        stage('Docker Compose Down') {
            steps {
                bat 'docker compose down'
            }
        }

        stage('Docker Compose Up') {
            steps {
                bat 'docker compose up -d'
            }
        }

        stage('Verificar') {
            steps {
                bat 'docker ps'
            }
        }
    }
}