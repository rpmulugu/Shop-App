
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
    
        stage ('Testing Code' ){
            steps {
            withMaven(maven: 'maven'){
            sh 'mvn test'
            }
            }
            } 
       
    }//stages main
} //pipeline
