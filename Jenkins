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