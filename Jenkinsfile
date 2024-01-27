pipeline {
    agent {
        docker { image 'ubuntu:20.04'}
    }
    stages {
        stage ('build') {
            steps {
                sh 'docker run -it --name=app nginx:20.04'
                sh 'pwd'
            }
            
        }
    }
}