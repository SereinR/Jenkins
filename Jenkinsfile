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
        echo 'Compiling Java program...'
        sh 'javac Hello.java'
      }
    }

    stage('Run') {
      steps {
        echo 'Running program...'
        sh 'java Hello'
      }
    }
  }

  post {
    success { echo 'Pipeline finished: SUCCESS ✅' }
    failure { echo 'Pipeline finished: FAILURE ❌' }
  }
}
