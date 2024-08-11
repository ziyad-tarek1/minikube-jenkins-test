pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: 'main', url: 'https://github.com/ziyad-tarek1/minikube-jenkins-test.git'
            }
        }
      /*  stage('Deploy to Minikube') {
            steps {
                kubernetesDeploy(
                    kubeconfigId: 'myminikube-cred2',
                    configs: 'pod.yaml',
                    enableConfigSubstitution: true
                )
            }
        }*/
    stage('Deploy') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }



    }
}