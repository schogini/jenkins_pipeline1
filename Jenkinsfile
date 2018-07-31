pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'
      }
    }
    stage('Test FE') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo "Testing.."'
            sh 'sleep 10'
          }
        }
        stage('Test UI') {
          steps {
            sh 'echo "Test2"'
            sh 'sleep 20'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying.."'
      }
    }
  }
}