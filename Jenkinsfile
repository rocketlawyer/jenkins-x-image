pipeline {
    agent {
        label "jenkins-jx-base"
    }
    stages {
        stage('Build and Push Release') {
            when {
                branch 'master'
            }
            steps {
                container('jx-base') {
                    sh "export VERSION=0.$BUILD_NUMBER && skaffold build -f skaffold.yaml"
                }
            }
        }
    }
}
