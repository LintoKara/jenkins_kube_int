pipeline {
    agent any
    environment {
        MY_KUBECONFIG = credentials('kubeconfig')
    }
    stages {
        stage('stage 1') {
            steps {
                bat "kubectl --kubeconfig $MY_KUBECONFIG get pods"
                bat "kubectl --kubeconfig $MY_KUBECONFIG apply -f deployment.yaml"
                bat "sleep 20s"
                bat "kubectl --kubeconfig $MY_KUBECONFIG get pods"
            }
        }
    }
}
