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
                sh 'sudo docker-compose -f docker-compose.yml up -d'
             }
         }
     }
}