pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 755 ./jenkins/testbuild.sh'
      }
    }
  }
  post {
    always {
      junit 'build/reports/test.xml'

    }

  }
}