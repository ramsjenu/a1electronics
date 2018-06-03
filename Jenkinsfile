pipeline {
  agent any
  stages {
    stage('Validation') {
      steps {
        sh 'mvn validate'
      }
    }
    stage('Compile') {
      steps {
        sh 'mvn compile'
      }
    }
    stage('package') {
      steps {
        sh 'mvn package'
      }
    }
    stage('End') {
      steps {
        echo 'Success'
      }
    }
  }
  environment {
    production = 'PROD'
  }
}