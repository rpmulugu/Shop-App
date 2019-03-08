
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
            sh 'mvn build'
            }
            }
            } 
       
    }//stages main
} //pipeline
