pipeline {
  agent any
  stages {
    stage('Is this run required') {
      steps {
        echo 'is this run'
      }
    }

    stage('Static Check') {
      parallel {
        stage('Static Check') {
          steps {
            echo 'static check'
          }
        }

        stage('Unit test') {
          steps {
            echo 'UNIT test'
          }
        }

      }
    }

    stage('QA') {
      steps {
        echo 'QA'
      }
    }

    stage('Summary') {
      steps {
        echo 'summary'
      }
    }

  }
}