pipeline {
    agent any
    
    stages {
        stage('Clean workspace') {
            steps{
                sh 'Clean workspace'
                deleteDir()        
            }
        }
    
        stage('Checkout source') {
            steps
            {
                sh 'Checkout source'
                checkout(
                    [$class: 'GitSCM', branches: [[name: '*/master']], 
                    doGenerateSubmoduleConfigurations: false, extensions: [], 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[url: 'https://github.com/MohamedLakhdari/Pipeline']]])     
            }
        }
    }
}
