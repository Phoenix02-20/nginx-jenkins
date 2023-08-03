pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                script {
                    echo "Hello"
                    //sh "sudo kubectl --kubeconfig=$Kubernetes apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/deployservice.yaml"
                    sh 'kubectl version --client'
                    sh 'kubectl get pods'
                    kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "Kubernetes")
                }
            }
        }
    }
}
