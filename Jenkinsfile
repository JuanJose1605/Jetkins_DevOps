pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Descarga el código del repo
                checkout scm
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
