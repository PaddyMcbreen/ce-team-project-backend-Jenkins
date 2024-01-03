pipeline {
  agent any
  stages {
    stage('Build') {
        
      steps {
        echo 'test build'
        // sh 'docker build -t learners-api:latest .'
        script {
                 app = docker.build("brandonjones085/test")    
                }
      }
    }
    // stage('Test') {
    //   steps {
    //     script {
    //       docker.image('ce-project-backend:latest').inside {
    //         sh 'docker run ce-project-backend:latest'
    //         // sh 'docker run ce-project-backend:latest your-test-command'
    //       }
    //     }
    //   }
    // }
    // stage('Push to Docker Hub') {
    //   steps {
    //     script {
    //       withCredentials([usernamePassword(credentialsId: 'dockerhub-password', passwordVariable: 'dckr_pat_TRhEww0kpUmWgtEhGJvNpZi5L1Q', usernameVariable: 'shenukacj')]) {
    //         docker.image('ce-project-backend:latest').withRegistry('https://index.docker.io/v1/', 'Docker Hub') {
    //           sh 'docker login -u $shenukacj -p $dckr_pat_TRhEww0kpUmWgtEhGJvNpZi5L1Q'
    //           sh 'docker push ce-project-backend:latest'
    //         }
    //       }
    //     }
    //   }
    // }
  }
}





