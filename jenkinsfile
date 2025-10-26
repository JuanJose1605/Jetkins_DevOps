pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Descarga el código del repo
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t mi-app .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker-compose up -d'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'docker ps'
                }
            }
        }
    }
}
