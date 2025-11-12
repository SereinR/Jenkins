pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps { checkout scm }
    }
    stage('Build Java') {
      steps {
        echo 'Compiling Java program...'
        sh 'javac Hello.java'
      }
    }
  }
  post {
    success { echo 'SUCCESS ✅' }
    failure { echo 'FAILURE ❌' }
  }
}
