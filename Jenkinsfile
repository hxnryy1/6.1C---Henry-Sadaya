pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
               
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running tests...'
               
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code...'
                
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
                
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging...'
               
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production...'
                
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
