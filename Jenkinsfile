pipeline {
     agent any
     
     stages {
         stage('Build') {
            steps {
                sh 'mvn install -DskipTests'
            }
         }
         stage('Deploy'){
             steps {
                sh 'sudo systemctl start docker'
                sh 'sudo docker build . -t springboot-docker-container'
                sh 'sudo docker build . -t mysql:5.7'
                sh 'sudo docker-compose up -d'
             }
         }
     }
}