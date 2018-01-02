//load the shared pipeline library
//define all environment variables
//define variables for execution stages

environment{
  execagent="master"
}
node(env.execagent){
  //Steps to be able to call pipeline methods
  concurrency: 1
  checkout scm
  
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
