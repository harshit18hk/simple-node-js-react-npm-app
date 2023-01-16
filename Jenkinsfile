pipeline {
    agent any
  
    options {
        skipStagesAfterUnstable()
    }
   
    
    stages {

         stage('Clone repository') { 
            steps { 
                script{
                    checkout scm
                }
            }
        }

        stage('Install dependencies') { 
            steps { 
                script{
                    sh  'npm i --force'
                }
            }
        }
        
        stage('Build') { 
            steps { 
                script{
                    sh  'ng build'
                }
            }
        }
        
      
    }
 }
