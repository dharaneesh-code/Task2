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
