pipeline {
    agent any 
    stages {
        stage ('Build') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage ('Docker build') {
            steps {
                script {
                    sh 'docker built -t newimage:v1 .'
                    sh 'docker images'
                    sh 'docker run -itd --name Container -P newimage:v1'
                    sh 'docker ps'
                }
            }
        }
    }
}
