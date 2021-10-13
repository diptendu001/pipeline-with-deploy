pipeline {
    agent any
    tools {
        maven 'maven-3.6'
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
                 sh "docker build --tag=webapp-hello ."
                 sh "docker tag webapp-hello diptendu001/test100:webapp-v1"
                 sh "docker push diptendu001/test100:webapp-v1"
                  }
        }
               
       }
}
  
