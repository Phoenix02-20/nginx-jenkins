pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    echo "Hello"
                    def kubeconfigPath = env.kubeconfig
                    echo "Kubeconfig: ${kubeconfigPath}"
                }
            }
        }
    }
}
