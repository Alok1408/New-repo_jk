pipeline {
    agent {
        docker { image 'ubuntu' }
    }
    stages {
        stage ('build') {
            steps {
                sh 'docker run -it --name=app ubuntu'
                sh 'pwd && ls'
                
            }
            
        }
    }
}