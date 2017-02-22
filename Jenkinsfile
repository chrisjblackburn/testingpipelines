pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'hello build1'
      }
    }
    stage('Testing') {
      steps {
        parallel(
          "Chrome": {
            echo 'testing in chrome'

          },
          "Firefox": {
            echo 'testing in firefox'

          },
          "Safari": {
            echo 'testing in safari'

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
