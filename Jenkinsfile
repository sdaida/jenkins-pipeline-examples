pipeline {
    agent {
        docker { image 'openjdk-7-jdk-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'java --version'
            }
        }
    }
}