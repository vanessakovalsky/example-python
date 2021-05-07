    node {
      agent any 
        stage('Clone sources') {
            git url: 'https://github.com/vanessakovalsky/example-python.git'
        }
        
        stage('Gradle build') {
            buildInfo = rtGradle.run rootDir: "./", buildFile: 'build.gradle', tasks: 'pylint'
        }
        stage('testcode') {
            steps {
                sh 'python src/main.py'
            }
        }
    }
