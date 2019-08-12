pipeline {
    agent any

    stages {

        stage('Build') {
            steps{
                sh './gradlew clean build'
            }
        }

        stage('Snyk Checking') {
            steps {
                snykSecurity(snykInstallation: 'snyk', snykTokenId: 'snyk-api-token', failOnIssues: false)
            }
        }
    }
}