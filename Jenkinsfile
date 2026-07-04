pipeline {
  agent any
  environment {
    BUILD_SUCCESS = "false"
  }

  stages{
    stage("Stage1"){
      steps{
        script {
          sh '''
          echo "Pipe-1"
          cat pipe1.txt
          '''
        env.BUILD_SUCCESS = "true"
        }
    
      }
    }
    stage("Stage2"){
      steps{
        sh '''
        echo "Pipe-2"
        cat pipe2.txt
        '''
      }
    }
    stage("Stage3"){
      when {
        environment name: 'BUILD_SUCCESS', value: 'false'
      }
      steps{
        sh '''
        echo "Pipe-3"
        cat pipe3.txt
        '''
      }
    }
  }
    
}
