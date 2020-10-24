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

    stage('now new stage') {
      steps {
        echo 'now new staging...'
      }
    }

    stage('confirm') {
      steps {
        input(message: 'sup', ok: 'yayaya', id: 'yo', submitter: 'me', submitterParameter: 'meme')
      }
    }

  }
}