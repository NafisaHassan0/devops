pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build Docker image
                docker.build('my-node-app')
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
                // Deploy to Kubernetes (replace with your deployment commands)
                sh 'kubectl apply -f kubernetes'
            }
        }
    }
}
