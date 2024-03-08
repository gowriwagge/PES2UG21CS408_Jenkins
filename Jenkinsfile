pipeline {
  agent any
  stages {
//    stage('Clone repository') {
//      steps {
//        checkout([$class: 'GitSCM',
//                  branches: [[name: '*/main']],
//                  userRemoteConfigs: [[url: 'https://github.com/AlphaQ6353/PES2UG21CS417_Jenkins']]]
//      }
//    }
    stage('Build') {
      steps {
        build 'PES2UG21CS408-1'
        sh 'ge main.cpp-o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure{
      error 'Pipeline failed'
    }
  }
}
