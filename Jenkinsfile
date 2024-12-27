pipeline {
  agent any
  environment{
    PYTHON_PATH='C:\Users\bhuva\AppData\Local\Programs\Python\Python311;C:\Users\bhuva\AppData\Local\Programs\Python\Python311\Scripts'
  }
  stages{
    stage('Checkout'){
      steps{
        checkout scm
      }
    }
  }
  stages('Build'){
    steps{
      bat '''
      set PATH=%PYTHON_PATH%;%PATH%
      pip install -r requirements.txt
      '''
    }
  }
  stage('SonarAnalysis'){
    environment{
      SONAR_TOKEN=credentials('tada-token')
    }
    steps{
      bat'''
      set PATH=%PYTHON_PATH%;%PATH%
      sonar-scanner -Dsonar.projectKey=tada ^ 
      -Dsonar.sources=. ^
      -Dsonar.host.url=http://192.168.218.233:9000 ^
      -Dsonar.token=%SONAR_TOKEN%
      '''
    }
  }
}
post{
  success{
    echo 'went well and good'
  }
  failure{
    echo 'failed'
    }
}
