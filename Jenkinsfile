pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'Echo "This is test stage"'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'This is build stage'
          }
        }

        stage('build parallel') {
          steps {
            echo 'parallel'
          }
        }

      }
    }

    stage('deploy to Test') {
      steps {
        echo 'deploy to test env'
      }
    }

  }
}