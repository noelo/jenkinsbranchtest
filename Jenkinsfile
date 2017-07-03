pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        timestamps() {
          echo 'FirstStep'
        }
        
        echo 'Second Step'
      }
    }
    stage('Build Stage') {
      steps {
        sh 'mvn package'
      }
    }
  }
}