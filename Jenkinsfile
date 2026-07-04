pipeline {
  agent any

  stages{
    stage("Stage1"){
      steps{
        sh '''
        echo "Pipe-1"
        cat pipe4.txt
        '''
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
      steps{
        sh '''
        echo "Pipe-3"
        cat pipe3.txt
        '''
      }
    }
  }
    
}
