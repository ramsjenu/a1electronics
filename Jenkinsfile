pipeline {
  agent any
  stages {
    stage('package') {
      steps {
        sh 'mvn package'
      }
    }
    stage('Artifact') {
      steps {
        archiveArtifacts(artifacts: 'a1ecommerce.war', onlyIfSuccessful: true)
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
