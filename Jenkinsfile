pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "buid"'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "test 1"'
          }
        }

        stage('test 2') {
          steps {
            sh 'echo "Test 2"'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'echo "Deploy"'
      }
    }

  }
}