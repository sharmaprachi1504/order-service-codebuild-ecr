pipeline {
    agent any
    tools {
            maven 'MAVEN_HOME'
           
        }

    stages {
        stage('Build') {
            steps {
               
                bat 'cd D:\\Download\\apache-maven-3.8.4-bin\\apache-maven-3.8.4\\bin & mvn install'
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
