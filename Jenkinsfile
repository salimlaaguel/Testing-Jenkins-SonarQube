pipeline {
    agent any
    stages {
        stage('Sonarqube') {
            environment {
                scannerHome = tool 'SonarQubeScanner'
            }
            
            steps {
               withSonarQubeEnv(installationName: 'SonarQubeScanner', credentialsId: 'SonarQube') {
                sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}
