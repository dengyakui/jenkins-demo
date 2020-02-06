pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
        sh 'touch surefire-reports/*.xml'
      }
    }

  }
  post {
    always {
      junit 'surefire-reports/**/*.xml'
    }

  }
}