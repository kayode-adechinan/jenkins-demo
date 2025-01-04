pipeline {
    agent any  // Use any available agent

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                sh 'node hello.js'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step (if needed)...'
            }
        }
    }
}
