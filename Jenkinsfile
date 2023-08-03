pipeline {
    agent any

    stages {
        stage('kubeconfig Path') {
            steps {
                //sh "sudo kubectl --kubeconfig=${KUBECONFIG}} apply -f /var/jenkins_home/workspace/nginx-test/deployservice.yaml"
                script {
                    echo "Hello"
                    //sh "sudo kubectl --kubeconfig=$Kubernetes apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/deployservice.yaml"
                    sh 'sudo kubectl version --client'
                    sh 'sudo kubectl get pods'
                    //kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "Kubernetes")
                //}
            }
        }
    }
}
