pipeline {
  agent {
    docker {
      image 'maven:3.6.3'
    }

  }
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            sh 'echo "Hello"'
          }
        }

        stage('java_version') {
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

    stage('version') {
      steps {
        sh 'mvn --version'
      }
    }

    stage('date') {
      steps {
        pwd(tmp: true)
        sh 'date D'
      }
    }

    stage('env_var') {
      steps {
        sh 'printenv'
      }
    }

  }
}