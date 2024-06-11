pipeline {
    agent any
    environment {
        DEPLOY_ENV = 'staging'
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
                // Add staging-specific build steps here
            }
        }
        stage('Test') {
            steps {
                echo "Testing for ${env.DEPLOY_ENV} environment"
                // Add staging-specific test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying to ${env.DEPLOY_ENV} environment"
                // Add staging-specific deploy steps here
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
