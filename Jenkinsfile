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
        sh '/Users/admin/tools/apache-maven-3.3.3/bin/mvn package'
      }
    }
    stage('Validate Stage') {
      steps {
        fileExists 'helloworld-1.0-SNAPSHOT.jar'
      }
    }
  }
}