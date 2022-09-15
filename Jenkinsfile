pipeline {
  agent {
    docker {
        image 'node:16-alpine'
        args '-p 3000:3000'
    }
  }
  environment {
    CI = 'true'
  }
  node (label: 'master') {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
  }
}