pipeline {
    agent any 
    stages {
        stage ('git checkout') {
            steps {
                git url
            }
        }
        stage ('Maven build') {
            steps {
                script{
                     sh 'mvn test'
                }
            }
        }

        stage ('mvn inetegration testing') {
            stpes {
                script {
                    sh 'mvn clean install'
                }
            }
        }
}
