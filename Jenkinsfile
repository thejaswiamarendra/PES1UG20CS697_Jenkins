pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'make -C spain'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh 'main/hello_exec'
        echo 'Test Stage Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
        
