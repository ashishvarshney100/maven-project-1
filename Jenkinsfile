pipeline {
    agent any 
    stages {
        stage('clean') {
	    steps {
		
		sh 'mvn clean'
	        }
	    }
	stage('test') {
	    steps {
		sh 'mvn test'
	    }
	    post {
              always {
	          junit keepLongStdio: true, testResults: 'target/surefire-reports/.*xml'
	      }
	    }
	}
	stage('deploy') {
	    steps {
		sh 'mvn package'
	    }
	}
     }
}
