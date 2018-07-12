pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mv clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mv test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'localMaven') {
                    sh 'mv deploy'
                }
            }
        }
    }
}
