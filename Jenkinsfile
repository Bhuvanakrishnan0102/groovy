node{
  stage{'build'){
    echo 'building'
  }
  stages('test'){
    echo 'testing'
  }
  if(currentBuild.result=='SUCCESS'){
    echo 'looks good'
  }else{
    echo 'failed'
  }
}
