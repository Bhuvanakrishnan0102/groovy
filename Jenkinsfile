node{
  stage('Build'){
    echo 'building'
  }
  stage('Test'){
    echo 'testing'
  }
  if(currentBuild.result=='SUCCESS'){
    echo 'looks good'
  }else{
    echo 'failed'
  }
}
