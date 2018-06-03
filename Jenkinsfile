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
        archiveArtifacts(artifacts: 'project/target/*war', onlyIfSuccessful: true)
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
