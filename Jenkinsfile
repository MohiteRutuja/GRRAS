pipeline {
	agent any 
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build & compile') {
	           steps {
			  sh '/home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/GRRAS.war /home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/webapps'
			}}	
}
}
