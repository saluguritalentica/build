pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
        junit 'build/report/test.xml'
      }
    }
  }
}