pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker login -u abdel2020 -p ${pass}'
                sh 'docker build . -t registry.gitlab.com/latestg1/jenkins'
                sh 'docker push registry.gitlab.com/latestg1/jenkins'
            }
        }
    }
}
