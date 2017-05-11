node('master') {
    stage('Clean workspace') {
        echo 'Clean workspace'
        deleteDir()        
    }
    
    stage('Checkout source') {
        echo 'Checkout source'
        checkout(
            [$class: 'GitSCM', branches: [[name: '*/master']], 
             doGenerateSubmoduleConfigurations: false, extensions: [], 
             submoduleCfg: [], 
             userRemoteConfigs: [[url: 'https://github.com/MohamedLakhdari/Pipeline']]])     
    }
}
