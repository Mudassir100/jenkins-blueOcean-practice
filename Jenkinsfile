pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''ls
date
            '''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test stage'
          }
        }

        stage('test parallel') {
          steps {
            echo 'test parallel'
          }
        }

      }
    }

    stage('prod') {
      steps {
        sh '''ls
echo "abc"'''
        sleep 3
      }
    }

  }
}