pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Install Python') {
            steps {
                 steps {
                    echo 'TEST'
                }
            }
        }

        stage('Run Script') {
            steps {
                // Execute the Python script
                sh 'python3 hello.py'
            }
        }
    }
}
