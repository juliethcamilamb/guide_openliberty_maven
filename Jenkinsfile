pipeline {
    agent any
    stages {
      stage('clone') {
        steps {
          git 'https://github.com/openliberty/guide-getting-started.git'
            }
        }
      stage('accesproject') {
        steps {
            bat 'cd guide-getting-started'
            }
        }
      stage('accessapp') {
        steps {
            bat 'cd start'
            }
        }
      stage('clean') {
        steps {
            bat 'mvn clean'
            }
        }
      stage('build') {
        steps {
            bat 'mvn package'
            }
        }
      stage('deploy') {
        steps {
            bat 'mvn liberty:run'
            }
        }
    }
}