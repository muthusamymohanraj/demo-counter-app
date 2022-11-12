pipeline {
    agent any
    stages {
        stage ('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/muthusamymohanraj/demo-counter-app.git'
            }
        }

        stage('maven test') {
            steps {
                script {
                    sh 'mvn test'
                }
            }
        }

        stage ('mvn inetegration testing') {
            steps {
                script {
                    sh 'mvn verify -DskipUnitTests'
                }
                
            }
        }
        stage ('maven build') {
            steps {
                script {
                    sh 'mvn clean install'
                }
                
            }
        }

        stage ('static code analysis') {
            steps {
                    withSonarQubeEnv(credentialsId: 'sonar-cred') {
                        sh 'mvn clean package sonar:sonar'
                }
            }
        }



        
    }
        
}

                        
