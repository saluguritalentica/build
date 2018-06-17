pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
      }
      post {
        always {
          junit 'build/reports/results.xml'

        }

      }
    }
  }
}