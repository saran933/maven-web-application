pipeline{
  
  agent any
  
  environment {
    ENV_NAME = "${env.GIT_COMMIT}"
    ENV_NAME1 = $GIT_COMMIT
  }
  
  stages{
    stage('Checkout code') {
       steps{
       git credentialsId: 'GitHub_Credentials', url: 'https://github.com/saran933/maven-web-application.git'       
       }
    }
    stage('get the checkout id'){
      steps {
        script {
           def test1 = env.GIT_COMMIT
           echo '$test1'
           echo 'ENV_NAME'
           echo 'ENV_NAME1'
        }   
      }
    }
    
  }
  

}
