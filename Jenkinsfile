pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'pip install pytest'
            }
        }
        stage('Build') {
            steps {
                bat 'python ops.py'
            }
        }
        stage('Test') {
            steps {
                bat 'python -m pytest'
            }
        }
    }
}
