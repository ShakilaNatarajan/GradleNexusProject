pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Process'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'Test'
          }
        }
        stage('error') {
          steps {
            echo 'Integration Test'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}