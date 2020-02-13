pipeline {
  agent {
    docker {
      image 'maven:3.6.3'
    }

  }
  stages {
    stage('Hello_version_os') {
      parallel {
        stage('Hello') {
          steps {
            sh 'echo "Hello"'
          }
        }

        stage('java_v') {
          steps {
            sh 'java -version'
          }
        }

        stage('check_unix') {
          agent any
          steps {
            isUnix()
          }
        }

      }
    }

    
	
	stage('check_unix') {
		agent any
        steps {
          isUnix()
		  sh 'echo "foo"'
        }
    }
	  
	stage('version') {
      steps {
        sh 'mvn --version'
      }
    }

    stage('date') {
      steps {
        pwd(tmp: true)
        sh 'date'
      }
    }

    stage('env_var') {
      steps {
        sh 'printenv'
      }
    }

  }
}