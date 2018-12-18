pipeline {
  agent {
    docker {
      image 'python'
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
        sh 'mkdocs build'
      }
    }
    stage('Test') {
      steps {
        sh 'ls -l _site/'
      }
    }
  }
}