pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
  }

  stages {
    stage('Say Hello') {
      agent any

      steps {
        sayHello 'Awesome Student!'
      }
    }
    
    stage('Unit Tests') {
      agent {
        label 'master'
      }
      steps {
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
      }
    }
    stage('build') {
      agent {
        label 'master'
      }
      steps {
        sh 'ant -f build.xml -v'
      }
      
    
    }
  }
}
