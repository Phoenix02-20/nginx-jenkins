pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    echo "Hello"
                    sh 'kubectl version --client'
                    sh 'kubectl get pods'
                    kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "kubeconfig")
                }
            }
        }
    }
}
