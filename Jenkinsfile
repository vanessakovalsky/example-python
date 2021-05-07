pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('testcode') {
            steps {
                sh 'python src/main.py'
            }
        }
    }
}
