pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build Docker image
                script {
                    docker.build('my-node-app')
                }
            }
        }
        stage('Test') {
            steps {
                // Run tests (if applicable)
                script {
                    // Add your test commands here
                }
            }
        }
        stage('Deploy') {
            steps {
                // Deploy to Kubernetes (replace with your deployment commands)
                script {
                    sh 'kubectl apply -f your_kubernetes_manifests_directory'
                }
            }
        }
    }
}
