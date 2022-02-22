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
  post {
    always {
      echo 'This will always run'
    }
    success {
      echo 'This will run only if successful'
    }
    failure {
      echo 'This will run only if failed'
    }
    unstable {
      echo 'This will run only if the run was marked as unstable'
    }
    changed {
      echo 'This will run only if the state of the Pipeline has changed'
      echo 'For example, if the Pipeline was previously failing but is now successful'
    }
  }
}