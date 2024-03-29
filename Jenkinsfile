pipeline {
    agent any
    
    environment {
        DOCKER_IMAGE = 'my-node-app:latest'
        KUBE_CONFIG = credentials('your_kube_config_credential_id')
    }

    stages {
        stage('Build') {
            steps {
                // Build Docker image
                script {
                    docker.build(DOCKER_IMAGE)
                }
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
                script {
                    // Configure Kubernetes context
                    withCredentials([file(credentialsId: 'your_kube_config_credential_id', variable: 'KUBECONFIG')]) {
                        sh 'export KUBECONFIG=$KUBECONFIG && kubectl apply -f kubernetes/deployment.yaml'
                        sh 'export KUBECONFIG=$KUBECONFIG && kubectl apply -f kubernetes/service.yaml'
                    }
                }
            }
        }
    }
}
