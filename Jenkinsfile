pipeline {
  agent {
    docker { image 'nginx:5.7' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'cd /usr/share/nginx/html'
        sh 'echo "Hello nginx" > index.html'
        
      }
    }
  }
}