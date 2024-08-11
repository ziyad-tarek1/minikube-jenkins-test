pipeline {
    agent any

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