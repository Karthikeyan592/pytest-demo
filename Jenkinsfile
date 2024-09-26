pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Karthikeyan592/pytest-demo.git']]])
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
