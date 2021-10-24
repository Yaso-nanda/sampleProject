pipeline {
     agent any
     
     stages {
         stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
         }
         stage('Deploy'){
             steps {
                sh 'sudo systemctl start docker'
                sh 'sudo docker build . -t springboot-docker-container'
                sh 'sudo docker-compose up -d'
             }
         }
     }
}