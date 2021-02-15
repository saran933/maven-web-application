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
        script {
           Test = sh(returnStdout: true, script: 'echo $GIT_COMMIT')
           Test1 = sh(returnStdout: true, script: 'echo $GIT_PREVIOUS_SUCCESSFUL_COMMIT')
        }   
      }
    }
     stage('code'){
      steps {
        sh "echo ${Test}" 
        sh "echo ${Test1}"
      }
    }
    
  }
  

}
