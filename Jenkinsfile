stage ('deploy to k8s'){
  agent {
    dockerfile {
      filename 'Dockerfile'
      reuseNode true // <- this is if you need to access the workspace
    }
  }
  steps {
    sh "create -f pod.yml"
  }
}