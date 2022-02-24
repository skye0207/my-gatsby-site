pipeline {
  agent any
  tools {nodejs "nodejs16.13.1"}
  stages {
    stage('Build') { 
      steps {
        sh 'npm install sharp@0.28.3 --save --registry=https://registry.npm.taobao.org'
        sh 'npm install --registry=https://registry.npm.taobao.org'
        sh 'npm run build'  
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