pipeline{
    agent any
    
    stages{
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
            steps{
                sh '''cp target/GRRAS.war /home/rutuja/Documents/Devops-Softwares/apache-tomcat-9.0.89/webapps

'''
        }}    
    }
}
