pipeline {
    agent any

    triggers {
        githubPush()
    }
    stages {
        stage('Build') {
            steps {
                // Use Maven to build the code
                sh 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Run unit tests
                sh 'mvn test'
                // Run integration tests
                sh 'integration-test-command'
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate SonarQube for code analysis
                sh 'sonarqube-command'
            }
        }
        stage('Security Scan') {
            steps {
                // Perform security scan
                sh 'security-scan-command'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy to staging server
                sh 'deploy-to-staging-command'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on staging
                sh 'integration-test-on-staging-command'
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy to production server
                sh 'deploy-to-production-command'
            }
        }
    }
  post{
        success{
            mail to: "sunerar007@gmail.com",
            subject: "Pipeline Status Email!",
            body: "Pipeline was successfully!!"
        }
    }
}
