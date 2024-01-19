pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
    // VALUES = credentials('secret-values')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t shenukacj/learners-api-dev:1.0.0 .'
      }
    }
    stage('Login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push shenukacj/learners-api-dev:1.0.0'
      }
    }
  }
  post {
    always {
      sh 'docker logout'
    }
  }
}

// 