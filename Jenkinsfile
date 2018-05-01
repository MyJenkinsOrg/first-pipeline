pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('FirstStage') {
      steps {
        echo "Hello ${params.Name}!"
        sh 'java -version'
      }
    }
  }
  environment {
    MY_NAME = 'MEENU'
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}