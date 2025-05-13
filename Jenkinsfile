pipeline {
    agent any

    environment {
        KUBECONFIG = '/root/.kube/config' // Path to your Kubernetes config
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Here you can define your build process (e.g., Docker build)
                    echo 'Building the application...'
                }
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    // Apply Kubernetes deployment and service files
                    sh 'kubectl apply -f deployment.yaml'
                    sh 'kubectl apply -f service.yaml'
                }
            }
        }
    }
}

