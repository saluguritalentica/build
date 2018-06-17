pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 755 ./jenkins/testbuild.sh'
        sh './jenkins/testbuild.sh'
        junit(testResults: '/reports/test.xml', allowEmptyResults: true, keepLongStdio: true)
      }
    }
  }
  post {
    always {
      archiveArtifacts(artifacts: 'reports/*.jar', fingerprint: true)
      junit 'reports/*.txt'

    }

  }
}