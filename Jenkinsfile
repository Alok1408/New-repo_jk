pipeline {
  agent {
    docker { image 'nginx' }
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