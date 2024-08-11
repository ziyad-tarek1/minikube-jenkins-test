pipeline {
    agent any

    environment {
        K8S_CRED_ID = 'myminikube-cred'
       // K8S_TOKEN_ID = 'k8s-token'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://github.com/ziyad-tarek1/minikube-jenkins-test.git'
            }
        }

        stage('Deploy to Minikube') {
            steps {
                withKubeConfig(credentialsId: "${env.K8S_CRED_ID}") {
                    sh 'kubectl apply -f pod.yaml'
                }
            }
        }
    }
}