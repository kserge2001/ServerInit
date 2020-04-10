pipeline {
    agent any
    tools {
        maven 'M2_HOME'
    }
    stages{
        stage('build') {
          steps {
           echo "Hello world"
           sh 'docker build'
          }
        }
        stage('maven clean') {
          steps {
           sh 'mvn clean'
          }
        }
        stage('Maven install') {
          steps {
           sh 'mvn install'
          }
        }
    
    }
}

