pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3001:3000 -p 5001:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Clean') {
            steps {
                sh 'echo Clean step'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Build step'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Test step'
            }
        }
    }
}

