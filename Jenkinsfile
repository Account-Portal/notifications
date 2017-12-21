node{
  stage('prep'){
  checkout scm
  concurrency : 2
  def me =sh (script:'lerna updated',returnStdout:true).trim()
  print me
  }
}
