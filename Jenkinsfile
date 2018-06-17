pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
      }
      post {
        always {
          junit '/var/lib/jenkins/workspace/*.xml'

        }

      }
    }
  }
}