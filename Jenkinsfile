pipeline {
  agent {
    docker {
      image 'maven:3.3.3'
      args 'mvn -version'
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