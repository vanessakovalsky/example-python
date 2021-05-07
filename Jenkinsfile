 pipeline {
      agent any 
      stages {
        stage('Clone sources') {
            steps {
                git url: 'https://github.com/vanessakovalsky/example-python.git'
            }
        }
        
        stage('Gradle build') {
            steps {
                buildInfo = rtGradle.run rootDir: "./", buildFile: 'build.gradle', tasks: 'pylint'
            }
        }
        stage('testcode') {
            steps {
                sh 'python src/main.py'
            }
        }
      }
 }
