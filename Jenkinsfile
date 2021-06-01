pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "build"'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "test"'
          }
        }
        stage('unit test') {
          steps {
            sleep 1
          }
        }
        stage('abc test') {
          steps {
            sh 'test abc'
          }
        }
      }
    }
    stage('uat') {
      steps {
        sh 'deloy uat'
      }
    }
  }
}