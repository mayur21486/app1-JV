pipeline {
  agent any
  stages {
    stage('First Stage of pipline as code') {
      steps {
        echo 'This is first Pipline as code by script'
      }
    }

    stage('Build Stage') {
      steps {
        echo 'Build by script'
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