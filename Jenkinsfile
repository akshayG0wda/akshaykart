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
		sh '/home/gamut/Distros/apache-maven-3.6.1/bin/mvn install'
	}
	    }
	stage('Deployment') {
	    steps {
		    mv target/gamutkart.war /opt/server/tomcat/webapps/akshaykart.war
	}
	}
    }
}
