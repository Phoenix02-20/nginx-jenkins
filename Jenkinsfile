pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    echo "Hello"
                    kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "kubeconfig")
                }
            }
        }
    }
}
