pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
        archiveArtifacts(fingerprint: true, artifacts: 'build/libs/**/*.jar')
      }
      post {
        always {
          junit '/var/lib/jenkins/workspace/*.xml'

        }

      }
    }
  }
}