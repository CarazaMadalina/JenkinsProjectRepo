pipeline {
    parameters {
      string defaultValue: 'main', description: 'The branch to checkout (default: main)', name: 'BRANCH'
    }

    agent any
    
    tools {
      maven "mvn3.8.4"
    }

    stages {
      stage('Hello') {
        steps {
            echo 'Hello World'
            echo "${BRANCH}"
            sh 'echo ${BRANCH}'
        }
      }

      stage('Execute shell') {
       agent {
        label 'built-in'
       }

       steps {
        sh 'ls'
        sh 'chmod +x File.sh'
        sh './File.sh'
       }
    }

    stage('Clean Workspace') {
      steps {
        cleanWs()
      }
    }
  }
}
