pipeline {
    agent any

    stages {
        stage('Deploy to Minikube') {
            steps {
                kubernetesDeploy(
                    kubeconfigId: 'myminikube-cred',
                    configs: 'pod.yaml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}