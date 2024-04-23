pipeline {
    agent any
    tools {
        maven 'maven-3.9.5'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -version'
                sh 'mvn -f pom.xml -B -DskipTests clean package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts....."
                    archiveArtifacts artifacts: '**/*.jar'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'mvn -f pom.xml test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
