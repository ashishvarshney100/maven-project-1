pipeline {
    agent any 
    stages {
        stage('Compile & clean') {
	    steps {
		sh 'printenv'
		sh 'clean compile'
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
	
