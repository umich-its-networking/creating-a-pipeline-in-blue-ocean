pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        input 'Continue?'
      }
    }
    stage('') {
      steps {
        sh 'echo foobar'
      }
    }
  }
}