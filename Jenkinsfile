pipeline {
  agent {
    docker { image 'nginx:5.6' }
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