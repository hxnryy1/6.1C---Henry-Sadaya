pipeline {
    agent any
    environment {
        PROJECT_NAME = 'MyProject'
    }

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
            echo 'Pipeline execution finished.'
        }
        success {
            emailext(
                to: 'henrysday22@gmail.com',
                subject: "${env.JOB_NAME} - Build #${env.BUILD_NUMBER} - ${currentBuild.currentResult}",
                body: """
                <p>Build succeeded.</p>
                <p>Check console output at <a href="${env.BUILD_URL}">${env.BUILD_URL}</a> to view the results.</p>
                """,
                mimeType: 'text/html',
                attachLog: true
            )
        }
        failure {
            emailext(
                to: 'henrysday22@gmail.com',
                subject: "${env.JOB_NAME} - Build #${env.BUILD_NUMBER} - ${currentBuild.currentResult}",
                body: """
                <p>Build failed.</p>
                <p>Check console output at <a href="${env.BUILD_URL}">${env.BUILD_URL}</a> to view the results.</p>
                """,
                mimeType: 'text/html',
                attachLog: true
            )
        }
    }
}

