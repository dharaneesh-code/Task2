pipeline{
  agent any

  stages {
  stage('Hello') {
    steps {
      echo 'Hello from jenkins pipeline'
    }
  }

  stage('Checkout') {
    steps {
      checkout scm
    }
  }

  stage('Build') {
    steps {
     sh 'echo "Test Build stage"'
    }
  }

  stage('Archive') {
    steps {
      sh 'echo "test run successful" > output.txt'
      archiveArtifacts artifacts:'output.txt'
    }
 


}
post {
  success {
    echo 'pipeline completed'
  }
  failure {
    echo 'pipeline failed'
  }
  }
}
