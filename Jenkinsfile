
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
         
        stage ('Deploy Code' ){
            steps {
            withMaven(maven: 'maven'){
            sh 'mvn deploy'
            }
            }
            } 
        
        
    }//stages main
} //pipeline
