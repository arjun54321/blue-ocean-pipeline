pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'Test State'
          }
        }

        stage('test parallel') {
          steps {
            echo 'I am Parallel test'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Production Deployment'
        sleep 10
      }
    }

  }
}