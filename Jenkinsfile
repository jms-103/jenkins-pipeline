pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
            }
        }
        stage('Build') {
            steps {
                sh 'chmod +x ./build.sh'
                sh './build.sh'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Simulating test command"'
            }
        }
    }
} 
