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
                script {
                    // Check if Python is already installed
                    def pythonInstalled = sh(script: 'command -v python3 || echo "not found"', returnStdout: true).trim()
                    if (pythonInstalled == "not found") {
                        // Install Python if not found
                        sh '''
                        echo "Python not found. Installing..."
                        apt-get update && apt-get install -y python3 python3-pip
                        '''
                    } else {
                        echo "Python is already installed: ${pythonInstalled}"
                    }
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
