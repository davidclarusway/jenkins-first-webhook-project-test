pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
                sh 'echo Integrating Jenkins Pipeline with GitHub Webhook using Jenkinsfile'
                sh 'javac HelloWorld.java'
                sh 'java HelloWorld'
            }
        }
        stage('package'){
            steps{
                sh 'echo creating artifact with maven'
            }
        }
    }
}
