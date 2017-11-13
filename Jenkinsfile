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
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
    }
  }
}
     
