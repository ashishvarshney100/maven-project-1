pipeline {
    agent any 
    stages {
        stage('clean') {
	    steps {
		sh 'printenv'
		sh 'mvn clean'
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
	
