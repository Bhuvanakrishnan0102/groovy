pipeline{
  agent any
  stages{
    stage('Built'){
      steps{
        echo " i am building"
      }
    }
    stage('test'){
      steps{
        echo "testing"
      }
    }
    stage('deploy'){
      steps{
        echo "deploying"
      }
    }
  }
  post{
    success{
      echo 'success'
    }
    failure{
      echo 'failure'
    }
  }
}

