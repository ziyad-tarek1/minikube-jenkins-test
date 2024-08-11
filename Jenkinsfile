pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://github.com/ziyad-tarek1/minikube-jenkins-test.git'
            }
        }
     
    stage('Deploy') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }



    }
}