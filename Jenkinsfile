pipeline {
  agent any
   tools {
    maven 'MavenForApp1'
     }
  stages {
    stage('Test Code') {
      steps {
        // mvn test
      }
    }

    stage('Build Stage') {
      steps {
        // mvn install
      }
    }

    stage('Deploy on Test Box') {
      steps {
        echo 'Code has deployed on Test Box'
      }
    }

    stage('Deploy on Prod Box') {
      steps {
        echo 'Code has deployed on Test Box'
      }
    }

  }
}
