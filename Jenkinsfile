pipeline {
    agent any
    tool {
        maven 'M2_HOME'
    }
    stages{
        stage('build') {
          steps {
           echo "Hello world"
          }
        }
        stage('maven clean') {
          steps {
           sh 'mvn clean'
          }
        }
        stage('build') {
          steps {
           echo "Hello world"
          }
        }
    
    }
}

