node{
  concurrency: 1
  checkout scm
  dir('pipelines') 
  {
        git url: 'https://github.com/Account-Portal/pipelines.git'
  }
  def pipeline = load './pipelines/common.groovy'
  pipeline.prep()
}
