pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS024-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
         sh 'g++ main2.cpp -o output'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
