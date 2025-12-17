pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Repo checked out'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh '''
                kubectl apply -f k8s/web1/deployment.yaml
                kubectl apply -f k8s/web1/service.yaml
                '''
            }
        }
    }
}
