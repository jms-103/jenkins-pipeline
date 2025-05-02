pipeline {
    parameters {
        string(name: 'BRANCH', defaultValue: 'main', description: '빌드할 git branch')
    }
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                echo "Building branch: ${params.BRANCH}"
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
