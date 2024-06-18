pipeline {
    agent any

    stages {
        stage('Clone-Repo') {
	    	steps {
	        	checkout scm
	    	}
        }
	stage('Build') {
		steps {
			sh 'mvn install'
		}
	}	
	stage('Deploy') {
	   steps {
		sh 'scp target/gamukart.war root@172.31.35.33:/home/tomcat/webapps'
	}
    }
}
}
