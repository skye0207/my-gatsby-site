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
        sh 'echo "Hello World"'
        sh 'npm install' 
        sh 'echo finished'
        sh 'll'
      }
    }
  }
}