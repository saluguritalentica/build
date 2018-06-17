pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 755 ./jenkins/testbuild.sh'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/testbuild.sh'
      }
    }
  }
  post {
    always {
      archiveArtifacts(artifacts: 'reports/*.jar', fingerprint: true)
      junit 'reports/*.xml'

    }

  }
}