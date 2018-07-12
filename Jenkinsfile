node('master') { 
    def mvnHome = tool name: 'localMaven'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
    
    stage ('Checkout SCM') {
        checkout scm
    } 
    stage ('Build') { 
        //sh 'mvn clean compile' 
        echo ''
    }
}
