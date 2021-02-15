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
     stage('Build Comparision'){
       when {
         expression{
         Test == Test1
         }
       }
      steps {
        sh "Both checkout version are same" 
      }
    }
     stage('Build Comparision 2'){
       when {
         expression{
         Test != Test1
         }
       }
# comparision       
      steps {
        script {
        try{
        sh "Both checkout version are different" 
        }
          catch (Throwable e){
            echo "Caught ${e.toString()}"
            currentBuild.result = "SUCCESS"
          }
        }
      }
    }
    
  }
  

}
