pipeline {
    agent any
    tools {
        maven 'maven-3.6.1'
    }
    stages {
       stage("VERSION")
         {
          steps {
             sh "mvn --version"
                }
         }
       
        stage("Clean and Package")
         {
          steps {
              sh "mvn clean package"
                }
         }
         
        stage("DEPLOY")
        { 
            steps {
                echo "Deploy code goes here"                
                sh "deploy.sh" 
            }
        }
               
       }
}
  
