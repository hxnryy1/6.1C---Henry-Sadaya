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
        success {
            echo 'Pipeline executed successfully!'
            mail to: 'henrysday22@gmail.com',
                 subject: "SUCCESS: Jenkins Pipeline - ${env.JOB_NAME}",
                 body: "The Jenkins pipeline '${env.JOB_NAME}' has completed successfully.\n\nCheck Jenkins for more details."
        }
        failure {
            echo 'Pipeline execution failed.'
            mail to: 'henrysday22@gmail.com',
                 subject: "FAILURE: Jenkins Pipeline - ${env.JOB_NAME}",
                 body: "The Jenkins pipeline '${env.JOB_NAME}' has failed.\n\nCheck Jenkins for more details."
        }
    }
}
