pipeline{

    agent any
     environment {
        PATH = "$PATH:/opt/maven/apache-maven-3.8.6/bin"
    }
    
    stages{
       
        stage("sonar quality check"){
       
            
            steps{
              script{
                withSonarQubeEnv(credentialsId: 'sonar-token') {
                sh 'mvn clean package sonar:sonar'
                 }
            
                }
            }
        }
    }
    
}
