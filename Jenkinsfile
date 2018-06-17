pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod 777 ./jenkins/testbuild.sh'
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/testbuild.sh'
      }
    }
    stage('result') {
      steps {
        junit(testResults: 'build/report/test.xml', allowEmptyResults: true)
      }
    }
  }
}