pipeline{
  
  agent any
  
  stages{
    stage('Checkout code') {
       steps{
       git credentialsId: 'GitHub_Credentials', url: 'https://github.com/saran933/maven-web-application.git'       
       }
    }
    stage('get the checkout id'){
      steps {
     sh 'echo $GIT_COMMIT' 
     sh 'echo $GIT_PREVIOUS_COMMIT' 
      sh 'echo $GIT_PREVIOUS_SUCCESSFUL_COMMIT' 
      sh 'echo $GIT_LAST_COMMIT'   
      }
    }
    
  }
  

}
