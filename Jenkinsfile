pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
         sh 'ant -f test.xml -v'
      }
    }
  }

  post {
    always {
      archive 'dist/*.jar'
    }
  }
}
     
