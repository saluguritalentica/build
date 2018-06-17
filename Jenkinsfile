pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'hello'
      }
    }
  }
  post {
    always {
      junit 'build/report/test.xml'

    }

  }
}