pipeline {
    agent any
    tools {
        Maven 'Maven_3.3.9' 
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(Maven : 'Maven_3.3.9') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(Maven : 'Maven_3.3.9') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(Maven : 'Maven_3.3.9') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
