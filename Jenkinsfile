 pipeline {
      agent any 
      stages {
        stage('Clone sources') {
            steps {
                git url: 'https://github.com/vanessakovalsky/example-python.git'
            }
        }
        
       stage('Compile') { // Compile and do unit testing
             tools {
               gradle 'installGradle'
             }
             steps {
               // run Gradle to execute compile and unit testing
               sh 'gradle pylint'
             }
           }
        stage('testcode') {
            steps {
                sh 'python src/main.py'
            }
        }
      }
 }
