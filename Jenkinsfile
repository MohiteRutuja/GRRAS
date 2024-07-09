pipeline {
    agent any
 
    stages {
        stage('Checkout'){
	   steps{	
		checkout scm
            }}
        stage('Compile and Build'){
            steps{
                sh '''/home/rutuja/Documents/Devops-Softwares/apache-maven-3.9.7/bin/mvn install
'''
            }}
          stage('Deployment'){
            steps { 
                sh '''cp target/GRRAS.war /home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/webapps
'''	
                }}
	 stage('Slack-Notification'){
	     steps{
		 slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#devops-slack', color: 'good', message: 'Welcome in Jenkins Slack  Integration for devops slack jobs', teamDomain: 'student', tokenCredentialId: 'slack'
        }}
    }}	    
	    
    

