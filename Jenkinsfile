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
    stage('Run stage') {
      steps {
        sh 'java -cp ./target/helloworld-1.0-SNAPSHOT.jar com.noc.test.App'
      }
    }
  }
}