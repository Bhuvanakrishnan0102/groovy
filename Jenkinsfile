node{
  stage{'Build'){
    echo 'building'
  }
  stages('Test'){
    echo 'testing'
  }
  if(currentBuild.result=='SUCCESS'){
    echo 'looks good'
  }else{
    echo 'failed'
  }
}
