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
		sh '/opt/maven/maven/bin/mvn install'
	}
	    }
	stage('Deployment') {
	    steps {
		    mv target/gamutkart.war /opt/server/tomcat/webapps/akshaykart.war
	}
	}
    }
}
