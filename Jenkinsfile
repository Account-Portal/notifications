//load the shared pipeline library
//define all environment variables
//define variables for execution stages
def PIPELINE_URL='https://github.com/Account-Portal/pipelines.git'
def PIPELINE_FILE='./pipelines/common.groovy'

node(env.execagent){
  
  //Steps to be able to call pipeline methods
  concurrency: 1
  checkout scm
  
  dir('pipelines') 
  {
        git url: PIPELINE_URL
  }
  def pipeline = load PIPELINE_FILE
  
  
  //Setup the pipeline and execute all the stages
  pipeline.setUp()
  pipeline.start()
  pipeline.tearDown()
}
