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
    stage('Deploy') {
      options {
        timeout(time: 30, unit: 'SECONDS') 
      }
      input {
        message "Which Version?"
        ok "Deploy"
        parameters {
            choice(name: 'APP_VERSION', choices: "v1.1\nv1.2\nv1.3", description: 'What to deploy?')
        }
      }
      steps {
        echo "Deploying ${APP_VERSION}."
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
