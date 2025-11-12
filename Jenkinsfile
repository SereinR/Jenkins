pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build Java') {
      steps {
         sh 'javac Hello.java'
      }
    }
    stage('Run') {
      steps {
         sh 'java Hello'
      }
    }
  }
  post {
    success { echo 'Pipeline finished: SUCCESS ✅' }
    failure { echo 'Pipeline finished: FAILURE ❌' }
  }
}
