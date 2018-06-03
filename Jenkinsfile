pipeline {
  agent any
  stages {
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
