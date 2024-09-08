pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven...'
               
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests with JUnit and integration tests using Selenium...'
               
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code using SonarQube...'
                
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan using OWASP ZAP...'
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to AWS EC2 instance using Ansible...'
               
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging using Selenium...'
                
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production on AWS EC2 instance using Ansible...'
                
            }
        }
    }
    post {
        always {
            emailext(
                to: 'henrysday22@gmail.com',
                subject: "Build status: ${currentBuild.currentResult}",
                body: "Build log is attached",
                attachLog: true
            )
        }
    }
}
