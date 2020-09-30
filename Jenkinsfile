pipeline {
    agent docker {
        image 'bitnami/kubectl:1.19.2'
        args '-v /root/.kube/config:~/.kube/config'
    }

    stages {
        stage('deploy') {
            steps {
                sh 'kubectl create -f .'
            }
        }
    }
}
