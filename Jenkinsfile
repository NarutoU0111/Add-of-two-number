pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/NarutoU0111/Add-of-two-number.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/NarutoU0111/Add-of-two-number.git'
                bat 'python sum.py'
            }
        }
        stage('Test') {
            steps {
                bat 'python -m pytest'
            }
        }
    }
}
