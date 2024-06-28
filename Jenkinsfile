pipeline {
    agent any
    
parameters {
  string defaultValue: 'DEV', description: 'ENVIRONMENT Values', name: 'ENVIRONMENT'
}
 
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
                script {
                    if ( env.ENVIRONMENT == 'QA' ){
        	sh '''cp target/GRRAS.war /home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/webapps
'''
        	echo "deployment has been done on QA!"
			 }
			else ( env.ENVIRONMENT == 'UAT' ){
                sh '''cp target/GRRAS.war /home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/webapps
'''
    		echo "deployment has been done on UAT!"
			}
			echo "deployment has been done!"
			
                }
        }}  
    }
}
