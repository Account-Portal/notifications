node{
  concurrency: 1
  checkout scm
  dir('pipelines') 
  {
        git url: 'https://github.com/Account-Portal/pipelines.git'
  }
  def pipeline = load 'common.groovy'
  pipeline.prep()
}
