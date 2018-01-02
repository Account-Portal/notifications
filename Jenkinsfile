//load the shared pipeline library
//define all environment variables
//define variables for execution stages
def execagent="master"
environment{
  something='here'
}
node(execagent){
  //Steps to be able to call pipeline methods
  concurrency: 1
  checkout scm
  print something
  dir('pipelines') 
  {
        git url: 'https://github.com/Account-Portal/pipelines.git'
  }
  def pipeline = load './pipelines/common.groovy'
  
  
  
  //Setup the pipeline and execute all the stages
  pipeline.setUp()
  pipeline.start()
  pipeline.tearDown()
}
