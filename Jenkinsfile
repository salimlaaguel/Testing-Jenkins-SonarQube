pipeline {
    agent any
    stages {
        stage('Sonarqube') {
            environment {
                scannerHome = tool 'SonarQubeScanner'
            }
            
            steps {
               withSonarQubeEnv(installationName: 'Production SonarQubeScanner', credentialsId: 'SonarQubeToken') {
                sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
}
