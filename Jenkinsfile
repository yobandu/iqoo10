pipeline {
	agent any
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/abhishek/apache-maven-3.9.5-bin/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			
			sh 'cp target/iqoo10.war /home/abhishek/apache-tomcat-9.0.82/webapps'
			}}
		stage('slack notification'){
		    steps {
			
			slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'devops-slack', color: 'good', message: 'welcome to jenkins', teamDomain: 'Abhishek Electricals', tokenCredentialId: '022a0d4a-fd06-4445-a08a-4813ec212e81'
			}}
			}}
