pipeline {
  agent {
    docker {
      image 'node:7-alpine'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh 'node --version'
      }
    }

  }
  post {
    always {
      junit 'surefire-reports/**/*.xml'
    }

  }
}