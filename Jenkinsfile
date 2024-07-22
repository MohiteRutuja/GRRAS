pipeline {
    agent{
	label 'slave-1'
	}
 
    stages {
        stage('Checkout'){
	   steps{	
		checkout scm
            }}
        stage('Compile and Build'){
            steps{
                sh '''JAVA_HOME=/home/grras/slavedir/jdk-11.0.23 /home/grras/slavedir/apache-maven-3.9.7/bin/mvn install
'''
            }}
          stage('Deployment'){
            steps { 
                sh '''cp target/GRRAS.war /home/grras/slavedir/apache-tomcat-9.0.89/webapps
'''	
                }}
    }}	    
	    
    

