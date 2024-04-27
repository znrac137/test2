 pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Build the code using Maven"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Run unit tests using JUnit"
                echo "Run integration tests using a tool like Selenium or Cucumber"
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Integrate a code analysis tool like SonarQube"
            }
        }
        stage('Security Scan') {
            steps {
                echo "Perform a security scan using a tool like OWASP ZAP or SonarQube"
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploy the application to a staging server using a tool like AWS CLI or Jenkins SSH plugin"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Run integration tests on the staging environment"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploy the application to a production server using a tool like AWS CLI or Jenkins SSH plugin"
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
