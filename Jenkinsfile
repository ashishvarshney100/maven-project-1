pipeline {
    agent any 
    stages {
        stage('Compile & clean') {
	    steps {
		sh 'echo "hello webhook configured"'

		sh 'mvn clean compile'
	        }
	    }
	stage('test') {
	    steps {
		sh 'mvn test'
	    }
	}
	stage('deploy') {
	    steps {
		sh 'mvn package'
	    }
	}
     }
}
