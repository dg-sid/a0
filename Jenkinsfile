pipeline {
  agent {
    docker {
      image 'maven:3.6.3'
    }

  }
  stages {
	stage ('Hello') {
	  steps {
	    sh 'echo "Hello"'
	  }
	}
    stage('build') {
      steps {
        sh 'mvn --version'
      }
    }

  }
}
