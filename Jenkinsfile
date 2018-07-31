pipeline {
  agent {
    node {
      label 'node1'
    }

  }
  stages {
    stage('Build Phase') {
      steps {
        sh 'echo "Building 123..."'
      }
    }
    stage('Test FE') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo "Testing.."'
            sh 'sss'
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