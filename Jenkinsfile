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

<<<<<<< HEAD
        stage('java_v') {
=======
        stage('java_version') {
>>>>>>> 5ed5cda86dc218717e1ec038c36d20b073ef4c7c
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
        sh 'date -rfc'
      }
    }

    stage('env_var') {
      steps {
        sh 'printenv'
      }
    }

  }
}