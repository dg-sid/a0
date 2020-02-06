pipeline {
  agent {
    docker {
      image 'maven:3.6.3'
      args 'mvn --version'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'mvn --version'
      }
    }

  }
}
