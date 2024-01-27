pipeline {
  agent {
    docker { image 'ubuntu:16.04' }
  }
  stages {
    stage('Test') {
      steps {
        sh '''cd /usr/share/nginx/html
            echo "hello-nginx" > index.html'''
        
      }
    }
  }
}