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
                bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=65ae3c9e182359c95aa2126fc0e94810732ba395 -Dsonar.organization=prachisharma01 -Dsonar.projectKey=Bench_practice_java'
            }
           // -Dsonar.version=5.6
        }
        stage('DockerImageBuild') {
            steps {
                bat 'docker build -t testimage .'
                bat 'docker run -d -p 8086:8080 testimage'
            }
        }
    }
}
