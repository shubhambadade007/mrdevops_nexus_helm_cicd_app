pipeline{

    agent any
    
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
