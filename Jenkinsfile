pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Clean') {
            steps {
                sh 'docker stop $(docker ps -q --filter ancestor=lamp_image)'
                sh 'docker rm -f $(docker ps -q --filter ancestor=lamp_image)'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t lamp_image ."
            }
        }
        stage('Test') {
            steps {
                sh 'docker run -d -p 80:80 -p 3306:3306 lamp_image"
            }
        }
    }
}

