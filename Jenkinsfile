pipeline{
  
  agent any
  
  stages{
    stage('Checkout code') {
       steps{
       git credentialsId: 'GitHub_Credentials', url: 'https://github.com/saran933/maven-web-application.git'       
       }
    }
    
  }
  

}
