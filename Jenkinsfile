pipeline {
  agent any
  environment {
    TEST_GLOBAL_VAR = 'testing global var'
  }

  stages {
    stage ('test vars')
    environment {
      TEST_LOCAL_VAR = 'testing local var'
    }
    steps {
      echo 'single global quotes:'
      echo '${TEST_GLOBAL_VAR}'
      echo "double global quotes:"
      echo "${TEST_GLOBAL_VAR}"
      
      echo 'single local quotes:'
      echo '${TEST_LOCAL_VAR}'
      echo "double local quotes:"
      echo "${TEST_LOCAL_VAR}"
    }
    
    stage ('test global lib')
    steps {
      testLib()
    }

  }
  post {
    always {
      echo 'post always'
    }

    success {
      echo 'post success'
    }

  }
}
