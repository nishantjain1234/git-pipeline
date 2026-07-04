pipeline {
  agent any
  environment {
    x= "false"
  }

  stages{
    stage("Stage1"){
      steps{
        sh '''
        echo "Pipe-1"
        cat pipe1.txt
        env.x= "true"
        '''
      }
    }
    stage("Stage2"){
      steps{
        sh '''
        echo "Pipe-2"
        cat pipe4.txt
        '''
      }
    }
    stage("Stage3"){
      when {
        environmentname: 'x', value: 'true'
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
