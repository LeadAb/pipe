pipeline {
    agent {
        dockerfile {
         filename 'Dockerfile'
         reuseNode true // <- this is if you need to access the workspace
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
