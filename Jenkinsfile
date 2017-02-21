pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'hello build1'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Chrome": {
            echo 'testing in chrome'

          },
          "Firefox": {
            echo 'testing in firefox'

          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }
  }
  environment {
    test = '123'
  }
}
