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
                sh 'sudo docker-compose -f docker-compose up -d'
             }
         }
     }
}