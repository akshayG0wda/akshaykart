pipeline 
{
    agent any

    stages 
	{
        	stage('Checkout') 
		{
            		steps 
			{
				checkout scm
			}
		}
		stage('Build') 
		{
			steps 
			{
				sh '/pythonAnsible/maven/bin/mvn install'
			}
		}
		stage('Deployment') 
		{
	    		steps 
			 {
				sh "sudo chmod 777 /pythonAnsible/tomcat/webapps"
		    		sh "mv /var/lib/jenkins/workspace/pipe2/target/gamutkart.war /pythonAnsible/tomcat/webapps/"
			 }    
		}
	}
}
