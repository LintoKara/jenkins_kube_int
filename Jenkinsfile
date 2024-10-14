pipeline {
    agent any
    stages {
        stage('stage 1') {
            steps {
                script {
                    withKubeConfig([credentialsId: 'kubeconfigfile']) {          
                    bat "kubectl  get pods"
                    bat "kubectl  apply -f deployment.yaml"
                    bat "kubectl  get pods"
                    }
                }
            }
        }
    }
}
