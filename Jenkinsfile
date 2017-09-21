pipeline {
  agent {
    docker {
      image 'node:6.11.2-stretch'
    }
    
  }
  stages {
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Start') {
      steps {
        sh 'npm start'
      }
    }
    stage('Arquivar') {
      steps {
        archiveArtifacts 'package.json'
      }
    }
  }
}