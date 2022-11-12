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
                    sh 'mvn clean install'
                }
                
            }
        }

        
    }
        
}

                        


