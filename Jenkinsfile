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
      }
    }

    stage('unit test') {
      steps {
        junit(testResults: '**/*.xml', allowEmptyResults: true)
      }
    }

  }
}