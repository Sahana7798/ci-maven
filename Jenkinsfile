pipeline {
    agent any
    tools {
        maven "mymaven"
    }
    stages {
        stage ('Git checkout') {
            steps {
               git 'https://github.com/Sahana7798/hello-world.git'

            }
        }
        stage ('unit testing') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('Integration testing') {
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }
        stage ('Maven build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
