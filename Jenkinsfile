pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : '/var/jenkins_home/maven/apache-maven-3.5.3/bin/') 
                {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : '/var/jenkins_home/maven/apache-maven-3.5.3/bin/') 
                {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : '/var/jenkins_home/maven/apache-maven-3.5.3/bin/') 
                {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
