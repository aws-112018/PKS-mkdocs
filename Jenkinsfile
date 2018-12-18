pipeline {
  agent {
    docker {
      image 'python:2.7'
      args '-v $WORKSPACE:/docs'
    }

  }
  stages {
    stage('Install') {
      steps {
        sh '''pip install mkdocs-material
'''
      }
    }
    stage('Build') {
      steps {
        sh '''echo pwd
#mkdocs build'''
      }
    }
    stage('Test') {
      steps {
        sh 'ls -l _site/'
      }
    }
  }
}