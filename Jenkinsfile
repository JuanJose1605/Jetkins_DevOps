pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Container') {
            steps {
                script {
                    // ✅ Usar Compose v2 (ya incluido en Docker moderno)
                    sh 'docker compose up -d'
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
