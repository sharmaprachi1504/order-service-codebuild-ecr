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
        stage('SonarAnalysis') {
            steps {
                bat 'sonar:sonar -Dsonar.host.url=https://sonarcloud.io -Dsonar.version=5.6 -Dsonar.login=ca8f7549be785d7880c59ce1ae6d4f0714b57abe -Dsonar.organization=narendrakumar02 -Dsonar.projectKey=narendrakumar02_BenchFreshersTrainingAssignment'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
