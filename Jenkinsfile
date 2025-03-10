pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS071-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh 'invalid_command'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
