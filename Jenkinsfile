pipeline {
  agent any

  environment {
    IMAGE_NAME = "demo-app"
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t $IMAGE_NAME .'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run --rm $IMAGE_NAME'
      }
    }
  }
}
