pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test steps'
          }
        }

        stage('Test par') {
          steps {
            echo 'Test par'
          }
        }

      }
    }

    stage('Depliy') {
      steps {
        echo 'Deploy on test'
        sleep 30
      }
    }

  }
}