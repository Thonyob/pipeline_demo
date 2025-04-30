pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo "jenkins file"
      }
    }
    stage('Test') {
      parallel{
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
    stage('Deploy'){
      steps{
        timeout(time: 60 , unit: 'SECONDS'){
          input(message: 'deploy', ok: 'hagasmolo')
        }
      }
  }
 }
}  
  
