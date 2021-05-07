pipeline {
    agent any 
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
