pipeline {
    agent any
    
    stages {
        stage('Clean workspace') {
            steps {
                deleteDir()        
            }
        }
    
        stage('Checkout source') {
            steps {
                checkout scm    
            }
        }
        
        stage('Build') {
            steps {
                sh 'ant build'
            }
        }
    }
}
