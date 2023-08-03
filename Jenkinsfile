pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    echo "Hello"
                    sh 'kubectl version --client'
                    kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "kubeconfig")
                }
            }
        }
    }
}
