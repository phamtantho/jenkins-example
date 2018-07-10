// Discard old builds
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '14', artifactNumToKeepStr: '10', daysToKeepStr: '14', numToKeepStr: '10'))])

node('master') {
    stage('Build'){
        def mvnHome = tool 'localMaven'           // define which maven tool used
        env.PATH = "${mvnHome}/bin:${env.PATH}"   // declare maven environment path
        sh 'mvn clean package'                    // build
    }
}
