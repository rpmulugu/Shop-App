
pipeline { 
    agent any
    
    stages {
        
        
      stage ('Compile Code' ){
            steps {
            withMaven(maven: 'maven'){
            sh 'mvn clean compile'
            }
            }
        }
    
      stage ('Package Code' ){
            steps {
            withMaven(maven: 'maven'){
            sh 'mvn package'
            }
            }
            } 
         
      stage("build & SonarQube analysis") {
          node {
              withSonarQubeEnv('My SonarQube Server') {
                 sh 'mvn clean package sonar:sonar'
              }
          }
      }

      
        
        
    }//stages main
} //pipeline
