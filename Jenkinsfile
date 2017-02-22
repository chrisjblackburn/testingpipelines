pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'hello build1'
        sleep '1'
        sh '''#/bin/bash
echo "Hello"'''
        echo 'Testing 123'
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

          },
          "Safari": {
            echo 'Safari'

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
