pipeline {
    agent any

    stages {
       stage('Clone-Repo') {
	  steps {
	        	git url: 'https://github.com/yunukolusuvarna/gamukart.git',
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
	        sh 'echo deploying application '
	    }
	}
}
}
