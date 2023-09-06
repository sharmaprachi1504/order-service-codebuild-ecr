pipeline {
    agent any
    tools {
            maven 'M2_HOME'
           
        }

    stages {
        stage('Build') {
            steps {
               
                bat 'mvn install'
            }
        }
        stage('SonarAnalysis') {
            steps {
                //bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=fd6f2d848a93fd3a81af15bcbd40efe0c915d754 -Dsonar.projectKey=Bench_Practice_Java'
            }
        }
        stage('DockerImageBuild') {
            steps {
                bat 'docker build -t testimage .'
                bat 'docker run -d -p 8089:8080 testimage'
            }
        }
    }
}
