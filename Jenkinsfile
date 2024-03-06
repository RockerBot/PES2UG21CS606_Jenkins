pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        build 'PES2UG21CS606-1'
        sh 'g++ main/hello.cpp -o output'
      }
    }
    stage('Test'){
      steps {
        build 'PES2UG21CS606-1'
        sh './output'
      }
    }
    stage('Deploy'){
      steps {
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
