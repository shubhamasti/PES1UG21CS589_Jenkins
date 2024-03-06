pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ new.cpp -o output'
        build 'PES1UG21CS589_1'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
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
