pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                dir('gs-maven') {
                    bat 'mvn clean test'
                }
            }
        }
    }

    post {
        success {
            echo '✅ Build and tests completed successfully.'
        }
        failure {
            echo '❌ Build failed. Check logs for details.'
        }
    }
}