pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                // Add build steps here
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running tests...'
                // Add testing steps here
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
                echo 'Performing security scan...'
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
                // Add staging tests here
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
