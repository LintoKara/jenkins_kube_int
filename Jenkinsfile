pipeline {
    agent any
    stages {
        stage('stage 1') {
            steps {
                script {
                    withKubeConfig([credentialsId: 'kubeconfig']) {          
                    bat "kubectl --kubeconfig $MY_KUBECONFIG get pods"
                    bat "kubectl --kubeconfig $MY_KUBECONFIG apply -f deployment.yaml"
                    bat "kubectl --kubeconfig $MY_KUBECONFIG get pods"
                    }
                }
            }
        }
    }
}
