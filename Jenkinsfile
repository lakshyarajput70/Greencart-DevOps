pipeline {
    agent any

    stages {

        stage('Verify Docker') {
            steps {
                bat 'docker --version'
            }
        }

        stage('Stop Existing Containers') {
            steps {
                bat 'docker compose down'
            }
        }

        stage('Pull Latest Images') {
            steps {
                bat 'docker compose pull'
            }
        }

        stage('Start Containers') {
            steps {
                bat 'docker compose up -d'
            }
        }

        stage('Check Running Containers') {
            steps {
                bat 'docker ps'
            }
        }
    }
}