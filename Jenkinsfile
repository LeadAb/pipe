pipeline {
    agent {
        docker {
        image 'bitnami/kubectl:latest'
        args '-v /root/.kube/config:/.kube/config'
        }
    }
    stages {
        stage('deploy') {
            steps {
                sh 'create -f pod.yml'
            }
        }
    }
}
