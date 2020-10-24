pipeline {
  agent any
  stages {
    stage('another test') {
      steps {
        echo 'testing...'
        echo 'testinggg'
        echo 'another testing,,,'
      }
    }

    stage('manual stage') {
      steps {
        echo 'now manual'
      }
    }

    stage('shell') {
      parallel {
        stage('shell') {
          steps {
            sh 'sh ./test.sh'
          }
        }

        stage('para') {
          steps {
            sh 'echo \'paralleling\''
          }
        }

      }
    }

  }
}