pipeline {
    agent any

    stages {
        stage('Build & Test') {
            steps {
                dir('gs-maven') { // 👈 change this to match your actual project folder
                    bat 'mvn clean test'
                }
            }
        }
    }
}