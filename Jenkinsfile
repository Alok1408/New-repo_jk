pipeline {

  environment {
    dockerimagename = "anaiik1708/reverso-pipeline-animals"
    BUILD_TAG = "1.0"
    dockerImage = ""
  }
  
  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git branch: 'main', credentialsId: 'github-key-reverso', url: 'git@github.com:Anaiik/docker-sample-pipeline-reverso.git'
      }
    }

    stage('Build image') {
      steps{
        script {
          dockerImage = docker.build "${env.dockerimagename}:${env.BUILD_TAG}"
        }
      }
    }

    stage('Pushing Image') {
      environment {
               registryCredential = 'dockerhublogin'
           }
      steps{
        script {
          docker.withRegistry( 'https://registry.hub.docker.com', registryCredential ) {
            dockerImage.push("${env.BUILD_TAG}")
          }
        }
      }
    }

    stage('Deploying App to Kubernetes') {
      steps {
        script {
          sh 'echo "need to run kubernetes cli here!!!"'
        }
      }
    }

  }
}