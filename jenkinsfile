pipeline {
    agent any
    environment {
        DEPLOY_ENV = 'preprod'
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
                // Add pre-production-specific build steps here
            }
        }
        stage('Test') {
            steps {
                echo "Testing for ${env.DEPLOY_ENV} environment"
                // Add pre-production-specific test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to ${env.DEPLOY_ENV} environment"
                // Add pre-production-specific deploy steps here
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
