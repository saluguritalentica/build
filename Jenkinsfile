pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
      }
      post {
        always {
          archiveArtifacts(artifacts: './jenkins/*.jar', fingerprint: true)
          junit 'build/report/*.xml'

        }

      }
    }
  }
}