pipeline {
    agent any
   
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
