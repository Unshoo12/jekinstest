pipeline {
  agent any
  stages {
    stage('Is this run required') {
      steps {
        git 'https://github.com/Unshoo12/jekinstest.git'
        build 'checkholidaydate'
      }
    }

    stage('Build') {
      steps {
        git 'https://github.com/Unshoo12/jekinstest.git'
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