pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 755 ./jenkins/testbuild.sh'
        sh './jenkins/testbuild.sh'
      }
    }
  }
  post {
    always {
      junit 'reports/*.xml'

    }

  }
}