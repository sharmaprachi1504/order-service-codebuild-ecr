pipeline {
    agent { label 'docker_agent'}
   // tools {
      //      maven 'MAVEN_HOME'
           
       // }

    stages {
        stage('Git Clone'){
            steps{
                sh 'git clone https://github.com/sharmaprachi1504/order-service-codebuild-ecr.git'
            }
        }
                
        stage('Build') {
            steps {
               
                sh 'cd order-service-codebuild-ecr && mvn install'
            }
        }
        stage('SonarAnalysis') {
            steps {
                sh 'cd order-service-codebuild-ecr && mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=fd6f2d848a93fd3a81af15bcbd40efe0c915d754 -Dsonar.projectKey=Bench_Practice_Java'
            }
        }
        //stage('DockerImageBuild') {
          //  steps {
              //  bat 'docker build -t testimage .'
              //  bat 'docker run -d -p 8090:8080 testimage'
           // }
       // }
    }
}
