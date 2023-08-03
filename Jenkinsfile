pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    def kubeconfigPath = env.KUBECONFIG
                    echo "Kubeconfig: ${kubeconfigPath}"
                }
            }
        }
    }
}
