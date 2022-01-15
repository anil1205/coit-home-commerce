pipeline {
    agent any

    stages {
        stage('Gitclone') {
            steps {
                git 'https://github.com/anil1205/coit-home-commerce.git'
                sh 'kubectl get pods'
            }
        }
        stage('deploy'){
            steps{
                 dir('kubernetes-manifests') {
                   sh 'kubectl apply -f    adservice.yaml'
}
            }
        }
    }
}
