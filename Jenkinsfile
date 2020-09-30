pipeline {
    agent {
        docker {
        image 'bitnami/kubectl:latest'
        args '-v /root/.kube/config:/.kube/config -v $PWD:/tmp'
        }
    }
    stages {
        stage('deploy') {
            steps {
                sh 'kubectl create -f /tmp/pod.yml'
            }
        }
    }
}
