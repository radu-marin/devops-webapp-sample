pipeline {
    agent {
        label "docker"
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
         stage('Clone repository') {
            steps {
                script{
                    checkout scm
                }
            }
        }
        stage('Build') {
            steps {
                script{
                    app = docker.build("devops-webapp-sample")
                }
            }
        }
    }
}
