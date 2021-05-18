pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Deploy') {
      steps {
        sh '''rsync -avz ./  \'.git\' /app
systemctl start nodeapp'''
      }
    }

  }
}