pipeline {
    agent any

    environment {
        IMAGE_NAME = "devops-demo"
        IMAGE_TAG = "build-${BUILD_NUMBER}"
    }

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        }

        stage('List Image') {
            steps {
                sh 'docker images'
            }
        }
    }
}
