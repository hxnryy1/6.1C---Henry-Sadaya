pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                // Add build steps here, e.g., sh 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running tests...'
                // Add test steps here
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code...'
                // Add code analysis steps here
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Scanning code for vulnerabilities...'
                // Add security scan steps here
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging...'
                // Add deployment steps here
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                // Add integration test steps here
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production...'
                // Add production deployment steps here
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
            mail to: 'henrysday22@gmail.com',
                 subject: "SUCCESS: Jenkins Pipeline - ${env.JOB_NAME}",
                 body: "The Jenkins pipeline '${env.JOB_NAME}' has completed successfully.\n\nCheck Jenkins for more details.",
                 attachLog: true
        }
        failure {
            echo 'Pipeline execution failed.'
            mail to: 'henrysday22@gmail.com',
                 subject: "FAILURE: Jenkins Pipeline - ${env.JOB_NAME}",
                 body: "The Jenkins pipeline '${env.JOB_NAME}' has failed.\n\nCheck Jenkins for more details.",
                 attachLog: true
        }
    }
}
