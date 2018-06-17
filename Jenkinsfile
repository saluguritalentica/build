pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 755 ./jenkins/testbuild.sh'
        sh 'chmod 755 /reports/'
      }
    }
  }
  post {
    always {
      junit 'reports/*.xml'

    }

  }
}