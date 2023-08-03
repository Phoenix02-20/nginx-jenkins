pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    def kubeconfigPath = env.kubeconfig
                    echo "Kubeconfig: ${kubeconfigPath}"
                }
            }
        }
    }
}
