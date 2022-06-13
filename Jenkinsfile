pipeline {
  agent any
   tools {
    maven 'MavenForApp1'
     }
  stages {
    stage('Test Code') {
      steps {
        // mvn test
        sh "mvn test"
      }
    }

    stage('Build Stage') {
      steps {
        // mvn install
        sh "mvn install"
      }
    }

    stage('Deploy on Test Box') {
      steps {
        echo 'Code has deployed on Test Box'
        deploy adapters: [tomcat9(credentialsId: 'testtom', path: '', url: 'http://192.168.122.36:8080/app-new')], contextPath: '/app-new', war: '**/*.war'
      }
    }

    stage('Deploy on Prod Box') {
      steps {
        echo 'Code has deployed on Test Box'
        deploy adapters: [tomcat9(credentialsId: 'prodtom', path: '', url: 'http://192.168.122.35:8080/app-new')], contextPath: '/app-new', war: '**/*.war'
      }
    }

  }
}
