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
		sh '/opt/maven/bin/mvn install'
	}
	    }
	stage('Deployment') {
	    steps {
		   // mv target/gamutkart.war /opt/apache/webapps/akshaykart.war
		    rm -rf target
	}
	}
    }
}
