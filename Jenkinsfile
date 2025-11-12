pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Build step…'
      }
    }
    stage('Test') {
      steps {
        echo 'Tests OK ✅'
      }
    }
  }

  post {
    success { echo 'Pipeline finished: SUCCESS' }
    failure { echo 'Pipeline finished: FAILURE' }
  }
}
