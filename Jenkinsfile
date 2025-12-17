pipeline {
    agent any

    environment {
        IMAGE_NAME = "web1-demo"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME ./app'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/web1'
            }
        }
    }
}
