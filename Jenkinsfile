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
                create -f pod.yml
            }
        }
    }
}
