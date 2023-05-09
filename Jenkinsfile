pipeline {
    agent any
    tools {
            maven 'MAVEN_HOME'
           
        }

    stages {
        stage('Build') {
            steps {
               
                bat 'mvn install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
