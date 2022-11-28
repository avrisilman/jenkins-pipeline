pipeline {
    agent any
   
    environment{
        PATH = "/opt/apache-maven-3.6.3/bin/mvn:$PATH"
    }
   
    stages {
        stage('Git') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/avrisilman/spring-cloud-contract'
            }
        }
         stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
