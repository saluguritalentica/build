pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
      }
      post {
        always {
          archiveArtifacts(artifacts: '*build/report/*.jar', fingerprint: true)
          junit 'build/report/*.xml'

        }

      }
    }
  }
}
