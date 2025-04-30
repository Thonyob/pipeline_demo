pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo "jenkins file"
      }
    }
    stage('Test') {
      paralell{
       stage('test Windows'){
        steps{
          echo "Run Windows"
        }
       }
       stage('test Linux'){
        steps{
          echo "Run Linux"
        }
       }
      }
    }
  }
}
