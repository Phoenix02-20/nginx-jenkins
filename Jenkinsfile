pipeline {
    agent any

    stages {
        stage('deployment') {
            steps {
                //sh "sudo kubectl --kubeconfig=${KUBECONFIG} apply -f /var/jenkins_home/workspace/nginx-test/deployservice.yaml"
                script {
                    echo "Hello"
                    //sh "sudo kubectl --kubeconfig=$Kubernetes apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/deployservice.yaml"
                    sh 'kubectl version --client'
                    sh 'kubectl get pods'
                    sh 'kubectl apply -f deployservice.yaml'
                }
            }
        }
    }
}
