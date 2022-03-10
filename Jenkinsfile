pipeline {
    parameters {
      string defaultValue: 'test', description: 'Param description', name: 'param'
    }


    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "${param}"
                sh 'echo ${param}'
            }
        }
    }
}