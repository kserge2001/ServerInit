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
          deploy adapters: [tomcat8(credentialsId: 'TomcatID', path: '', url: 'http://34.201.107.82:8080/')], contextPath: null, war: '**/*war'
          }
        }
        stage('Maven install') {
          steps {
           sh 'mvn install'
          }
        }
    
    }
    post {
        always {
            echo "always post this"
         }
        failure {
            echo "this job failed"
        }
    
    }
    
}

