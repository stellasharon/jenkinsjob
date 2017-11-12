pipeline {
  agent any

  environment {
    MAJOR_VERSION = 1
  }

  stages {
    stage('Say Hello') {
      steps {
        sayHello 'Awesome Student!'
      }
    }
    stage('Build') {
      steps {
         sh 'ant -f test.xml -v'
      }
    }
  }
}
     
