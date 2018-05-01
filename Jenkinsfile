pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('FirstStage') {
      steps {
        echo "Hello ${MY_NAME}!"
        sh 'java -version'
      }
    }
  }
  environment {
    MY_NAME = 'MEENU'
  }
}