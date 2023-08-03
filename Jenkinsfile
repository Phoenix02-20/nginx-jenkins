pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('dockerhub')
    }
    stages {
        stage ('Build Image') {
            steps {
                sh 'docker build -t priya20xenonstack/nginx-kube .'
            }
        }
        stage ('hub login') {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }
        stage ('Image Push') {
            steps {
                sh 'docker push priya20xenonstack/nginx-kube'
            }
        }
      
        stage('Deploying the Application to the K8s Cluster') {
          steps {
            //sh "sudo kubectl --kubeconfig=${KUBECONFIG} apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/drupal-secret.yaml"
            //sh "sudo kubectl --kubeconfig=${KUBECONFIG} apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/persistentvolumeclaim.yaml"
            //sh "sudo kubectl --kubeconfig=${KUBECONFIG} apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/drupal.yaml"
            //sh "sudo kubectl --kubeconfig=${KUBECONFIG} apply -f /var/lib/jenkins/workspace/jenkins-kubernetes/mysql-drupal.yaml"
              script {
                kubernetesDeploy(configs: "deployservice.yaml", kubeconfigId: "kubeconfig")
                sh "kubectl get pods"
              }
      }
     }
    }
    post {
       always {
           sh 'docker logout'
       } 
    }
}
