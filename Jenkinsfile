pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://github.com/ziyad-tarek1/minikube-jenkins-test.git'

            }
        }
    }


    stages {
        stage('Deploy to Minikube') {
            steps {
                kubernetesDeploy(
                    kubeconfigId: 'myminikube-cred2',
                    configs: 'pod.yaml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}