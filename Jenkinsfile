pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Confirm build') {
      steps {
        input 'Build?'
      }
    }
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        input 'Continue?'
        echo 'hi'
      }
    }
    stage('Echo') {
      steps {
        sh 'echo foobar'
      }
    }
    stage('Check') {
      steps {
        input 'Continue again?'
      }
    }
  }
}