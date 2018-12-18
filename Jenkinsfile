pipeline {
  agent {
    docker {
      args '-v $WORKSPACE:/docs'
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
        sh '''pwd
ls
mkdocs build'''
      }
    }
    stage('Test') {
      steps {
        sh 'ls site/'
      }
    }
  }
}
