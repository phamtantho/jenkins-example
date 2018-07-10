pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                //withMaven(maven : 'localMaven/bin') 
                {
                def mvnHome = tool 'localMaven'
                env.PATH = "${mvnHome}/bin:${env.PATH}"
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                //withMaven(maven : 'localMaven/bin') 
                {
                def mvnHome = tool 'localMaven'
                env.PATH = "${mvnHome}/bin:${env.PATH}"
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                //withMaven(maven : 'localMaven/bin') 
                {
                def mvnHome = tool 'localMaven'
                env.PATH = "${mvnHome}/bin:${env.PATH}"
                    sh 'mvn deploy'
                }
            }
        }
    }
}
