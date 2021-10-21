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
                sh 'docker-compose build'
                sh 'docker-compose up -d'
             }
         }
     }
}