pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG22CS144-1'
        sh 'cd main && g++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh 'cd main && ./output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline failed :('
    }
  }
}
