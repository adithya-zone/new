pipeline {
 agent any
 tools { maven 'Maven3' }
 stages {
  stage('Checkout'){ steps { checkout scm } }
  stage('Build'){ steps { sh 'mvn clean package' } }
  stage('Archive'){ steps { archiveArtifacts artifacts: 'target/*.war', fingerprint: true } }
 }
}