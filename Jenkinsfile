pipeline {
 agent any

 stages {

  stage('Build') {
   steps {
    sh 'mvn clean package'
   }
  }
 stage('Package') {
   steps {
    sh 'mvn package'
   }
  }

 }

 post {
  success {
   archiveArtifacts artifacts: 'target/*.jar'
  }
 }
}
