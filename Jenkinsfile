pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "test"'
      }
    }

    stage('Deploy') {
      steps {
        sh 'npm install'
      }
    }

  }
}