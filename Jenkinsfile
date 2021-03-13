pipeline {
  agent any
  stages {
    stage('Is this run required') {
      steps {
        git(url: 'https://github.com/Unshoo12/jekinstest.git', branch: 'testjen', changelog: true)
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