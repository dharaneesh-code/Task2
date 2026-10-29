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

  stage('Test') {
    steps {
      sh 'echo "test run successful"'
    }
  }
    stage('Archive Artifacts') {
       steps {
        sh 'echo "first artifacts" > output.txt'
        archiveArtifacts artifacts:'output.txt',
              
  }
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
