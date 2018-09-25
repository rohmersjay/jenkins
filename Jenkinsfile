pipeline {
       agent any
    tools {
        maven 'apache-maven-3.3.9'
        jdk 'jdk8'
    }
    agent any
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
