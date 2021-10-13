pipeline {
    agent any
    tools {
        maven 'mvn-3.6.3'
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
//              sh "docker build --tag=webapp-hello ."
//              sh "docker tag webapp-hello diptendu001/test100:webapp-v1"
//              sh "docker push diptendu001/test100:webapp-v1"
                sh "podman build -t docker.io/webapp-demo:v1 ."
                sh "podman -t docker.io/webapp-demo:v1 diptendu001/test100:webapp-demo-131021
                sh "podman push docker.io/diptendu001/test100:webapp-demo-131021
                  }
        }
 
     
    
               
       }
}
  
