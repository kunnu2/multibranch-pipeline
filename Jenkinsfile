pipeline {
    agent any
    environment {
        DEPLOY_ENV = 'production'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Building for ${env.DEPLOY_ENV} environment"
                // Add production-specific build steps here
            }
        }
        stage('Test') {
            steps {
                echo "Testing for ${env.DEPLOY_ENV} environment"
                // Add production-specific test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to ${env.DEPLOY_ENV} environment"
                // Add production-specific deploy steps here
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
