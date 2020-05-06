pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
		checkout scm
	    }
	}
	stage('Build') {
	    steps {
		sh '/pythonAnsible/maven/bin/mvn install'
	}
	    }
	stage('Deployment') {
	    steps {
		    mv /var/lib/jenkins/workspace/devMaster/pipeline e/target/gamutkart.war /pythonAnsible/tomcat/webapps/akshaykart.war
	    }    
	}
    }
}
