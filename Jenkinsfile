node{
  stage('Build'){
    echo 'building'
  }
  stage('Test'){
    echo 'testing'
  }
  if(currentBuild.currentResult=='SUCCESS'){
    echo 'looks good'
  }else{
    echo 'failed'
  }
}
