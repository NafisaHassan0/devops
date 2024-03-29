pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build Docker image
                sh 'docker build -t my-node-app .'
            }
        }
        stage('Test') {
            steps {
                // Run tests (if applicable)
                // Add your test commands here
            }
        }
        stage('Deploy') {
            steps {
                // Deploy to Kubernetes
                sh 'kubectl apply -f kubernetes'
            }
        }
    }
}
