pipeline {
    parameters {
        string(name: 'BRANCH', defaultValue: 'main', description: '빌드할 git branch')
    }
    // agent { label 'docker-builder' }
    agent any
    stages {
        stage('Checkout') {
            // agent { label 'windows-builder'}
            steps {
                echo 'Checking out code...'
                git url: 'https://github.com/jms-103/jenkins-pipeline', branch: params.BRANCH
                echo "소스코드를 Git 저장소에서 성공적으로 가져왔습니다."
            }
        }
        stage('Setup') {
            steps {
                echo "Python 환경을 설정합니다."
                echo "Python 환결설정 완료. (pytest 설치 완료)"
            }
        }
        stage('Test') {
            steps {
                echo 'pytest를 사용해서 테스트를 실행합니다.'
                sh 'pytest'
                echo '테스트 완료'
            }
        }
    }
} 
