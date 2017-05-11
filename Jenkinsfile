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
                checkout(
                    [$class: 'GitSCM', branches: [[name: '*/master']], 
                    doGenerateSubmoduleConfigurations: false, extensions: [], 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[url: 'https://github.com/MohamedLakhdari/Pipeline']]])     
            }
        }
        
        stage('Build') {
            steps {
                sh 'ant build'
            }
        }
    }
}
