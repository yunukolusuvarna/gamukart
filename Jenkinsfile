pipeline {
    agent any

    stages {
        stage('Clone-Repo') {
	    	steps {
	        	git url: 'https://github.com/Tharun4153/gamukart.git',
				branch: 'master'
	    	}
        }
	stage('Build') {
		steps {
			sh 'mvn install'
		}
	}	
	stage('Deploy') {
	   steps {
		sh 'scp target/gamutkart.war root@172.31.35.33:/opt/tomcat/webapps'
	}
    }
}
}
