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
        sh '''rsync -avz . /app/
sudo systemctl restart nodeapp'''
      }
    }

    stage('post') {
      steps {
        emailext(subject: 'test from jenkins', body: 'test email', from: 'dev@iwdt.com.jo', to: 'aqader@iwdt.com.jo')
      }
    }

  }
}