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
            bat(script: 'java -version', returnStdout: true)
          }
        }

        stage('check_unix') {
          steps {
            isUnix()
          }
        }

      }
    }

    stage('Mvn_version') {
      parallel {
        stage('version') {
          steps {
            sh 'mvn --version'
          }
        }

        stage('version_w') {
          steps {
            bat(script: 'mvn -v', returnStdout: true)
          }
        }

      }
    }

    stage('date') {
      steps {
        pwd(tmp: true)
        sh 'date -rfc'
      }
    }

  }
}